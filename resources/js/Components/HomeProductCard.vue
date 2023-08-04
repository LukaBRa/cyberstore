<script setup>

const props = defineProps(['product']);

</script>

<template>

<div class="home-product-card col-lg-2 col-md-4 col-12">

    <div class="card-header">
        <p>{{ product.category }}</p>
        <button class="card-save-btn"><i class="fa-regular fa-heart"></i></button>
    </div>

    <div class="product-image">
        <img src="/images/homepage/monitor-card.png" alt="Product">
    </div>

    <div class="product-info">
        <div class="rating">
            <i class="fa-solid fa-star yellow-rating"></i>
            <i class="fa-solid fa-star"></i>
            <i class="fa-solid fa-star"></i>
            <i class="fa-solid fa-star"></i>
            <i class="fa-solid fa-star"></i>
        </div>
        <a href="#" class="product-name">{{ product.name }}</a>
    </div>

    <div class="product-price mt-4">
        <p class="price"> $ {{ product.price }}</p>
        <button class="add-to-cart-btn"><i class="fa-solid fa-cart-plus"></i></button>
    </div>

</div>

</template>

<style>

.home-product-card {
    border-radius: 5px;
    padding: 0.5rem;
}

.card-header{
    display: flex;
    align-items: baseline;
    justify-content: space-between;
    color: #acacac;
}

.card-save-btn{
    border: none;
    background: none;
    color: #acacac;
    transition: all 0.3s ease;
    font-size: 1.1rem;
}

.card-save-btn:hover{
    color: var(--blue);
}

.fa-star{
    color: #acacac;
}

.yellow-rating{
    color: rgb(243, 207, 46);
}

.product-name{
    font-weight: bold;
    text-decoration: none;
    color: var(--dark);
    transition: all 0.3s ease;
}

.product-name:hover{
    text-decoration: underline;
}

.product-price{
    display: flex;
    align-items: baseline;
    justify-content: space-between;
}

.price{
    font-weight: bold;
    font-size: 1.2rem;
}

.add-to-cart-btn{
    color: var(--dark);
    border: 1px solid var(--dark);
    border-radius: 50%;
    padding: 0.3rem 0.5rem;
    background-color: white;
    transition: all 0.3s ease;
}

.add-to-cart-btn:hover{
    color: white;
    background-color: var(--blue);
    border: 1px solid var(--blue);
}

.product-image{
    margin: 2rem 0rem;
}

.product-image > img{
    height: 100%;
    width: 100%;
    object-fit: contain;
}

</style>