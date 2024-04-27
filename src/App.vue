<template>
  <FoodHeader/>
  <FoodCategories/>
  <FoodItemsList :foodItemsList = foodItemsList />
</template>

<script>
  import FoodHeader from "./components/FoodHeader.vue";
  import FoodCategories from "./components/FoodCategories.vue";
  import FoodItemsList from "./components/FoodItemsList.vue";

  export default{
    name:"App",
    components:{
      FoodHeader,
      FoodCategories,
      FoodItemsList
    },
    data(){
      return{
        foodItemsList:[]
      }
    },
    methods:{
      async fetchFoodDetails(){
        const res = await fetch("https://restaurant-zjxo.onrender.com/api");
        const foodData = await res.json();
        console.log(foodData);
        return foodData[0].foodItems;
      }
    },
    async created(){
      this.foodItemsList = await this.fetchFoodDetails();
    }
  }
</script>

<style scoped>
  @import url('https://fonts.googleapis.com/css2?family=Alice');

  *{
    font-family: "Alice", serif;
  }

</style>