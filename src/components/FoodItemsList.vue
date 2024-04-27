<template>
    <div>
        <div v-for="foodItem of foodItemsList" :key=foodItem.foodItem_id>
            <FoodItem :foodItem = foodItem />
        </div>
    </div>
</template>

<script>
    import FoodItem from "./FoodItem.vue";

    export default{
        name:"FoodItemsList",
        components:{
            FoodItem
        },
        props:{
            foodItemsList: Array
        }
    }
</script>

<style scoped>
</style>