<template>
    <div class="categories-container">
        <div>
            <img class="food-categories-icon" src="https://img.icons8.com/?size=48&id=psWZVEOb_nFK&format=png" alt="Appetizers Icon"/>
            <h4>Appetizers</h4>
        </div>
        <div>
            <img class="food-categories-icon" src="https://img.icons8.com/?size=48&id=SENAO5gAbChk&format=png" alt="Main course Icon"/>
            <h4>Main Course</h4>
        </div>
        <div>
            <img class="food-categories-icon" src="https://img.icons8.com/?size=48&id=24467&format=png" alt="Rice & Bread Icon"/>
            <h4>Naans</h4>
        </div>
        <div>
            <img class="food-categories-icon" src="https://img.icons8.com/?size=80&id=2dxqbvXO4Y8m&format=png" alt="Biryani Icon"/>
            <h4>Biryani</h4>
        </div>
        <div>
            <img class="food-categories-icon" src="https://img.icons8.com/?size=48&id=Eq5aUzFk6RKG&format=png" alt="Desserts Icon"/>
            <h4>Desserts</h4>
        </div>
        <div>
            <img class="food-categories-icon" src="https://img.icons8.com/?size=48&id=12863&format=png" alt="Beverages Icon"/>
            <h4>Beverages</h4>
        </div>
    </div>
</template>

<script>
    export default{
        name:"FoodCategories"
    }
</script>

<style scoped>
    .categories-container{
        display:flex;
        justify-content:space-evenly;
        align-items:center;
    }
    .food-categories-icon{
        border:transparent;
        border-radius:50%;
        box-shadow: 0px 0px 10px rgba(0, 0, 0, 0.5);
        padding:10px;
        width:40px;
        height:40px;
    }
</style>