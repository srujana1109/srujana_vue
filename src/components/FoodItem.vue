<template>
    <div>
        <h2 class="category-heading">{{foodItem.foodItem_category}}</h2>
        <div class="food-details">
            <div v-for=" item of foodItem.foodItems_items" :key=item.item_id class="food-item">
                <div id="food-item">
                    <img :src=item.item_image class="food-image"/>
                </div>
                <h3 class="item-name">{{item.item_name}}</h3>
                <div class="flex-container">
                    <p id="price">${{item.item_price}}</p>
                    <p><img src="https://img.icons8.com/?size=15&id=zX00FT5x6S7M&format=png" alt="star" />&nbsp;{{item.item_rating}}</p>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
    export default{
        name:"FoodItem",
        props:{
            foodItem:Object
        }
    }
</script>

<style scoped>
    .food-details{
        display:grid;
        grid-template-columns: auto auto auto;
        gap: 1em;
        font-size: 1.2em;
    }
    .flex-container{
        display:flex;
        justify-content:space-between;
        align-items:center;
        padding: 0em 1em;
    }
    .item-name{
        text-align:left;
        padding:0 1em;
    }
    .food-image{
        width:490px;
        height:250px;
        object-fit: cover;
    }
    .category-heading{
        text-align: center;
    }
    #price{
        font-size: 1.2em;
    }
</style>