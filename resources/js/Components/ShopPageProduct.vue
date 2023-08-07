<script setup>



</script>

<template>
<div class="col-lg-4 col-sm-6 col-12">
    <div class="shop-page-product">

        <div class="shop-page-product-head">
            <p>Laptop</p>
            <button><i class="fa-regular fa-heart"></i></button>
        </div>
        <div class="shop-page-product-image">
            <img src="/images/homepage/monitor-card.png" alt="Product">
        </div>
        <div class="shop-page-product-description">
            <div class="rating">
                <i class="fa-solid fa-star"></i>
                <i class="fa-solid fa-star"></i>
                <i class="fa-solid fa-star"></i>
                <i class="fa-regular fa-star"></i>
                <i class="fa-regular fa-star"></i>
            </div>
            <a href="" class="shop-page-product-name">
                LG Monitor 24 IPS 24BK750Y-B
            </a>
            <div class="shop-page-product-price">
                <p class="price">$240</p>
                <button class="shop-page-product-btn"><i class="fa-solid fa-cart-plus"></i></button>
            </div>
        </div>

    </div>
</div>

</template>

<style scoped>

.shop-page-product{
    border: 1px solid var(--light-gray);
    padding: 0.5rem;
}

.shop-page-product-head{
    display: flex;
    align-items: baseline;
    justify-content: space-between;
    color: rgb(175, 174, 174);
}

.shop-page-product-head button{
    background: none;
    border: none;
    color: rgb(175, 174, 174);
    transition: all 0.3s ease;
}

.shop-page-product-head button:hover{
    color: var(--blue);
}

.shop-page-product-image img{
    width: 100%;
    height: 100%;
    object-fit: contain;
}

.rating .fa-solid{
    color: rgb(238, 238, 41);
}

.shop-page-product-name{
    display: block;
    width: 100%;
    color: var(--dark);
    text-decoration: none;
    font-size: 1.1rem;
    font-weight: bold;
    margin-top: 0.5rem;
}

.shop-page-product-name:hover{
    text-decoration: underline;
}

.shop-page-product-price{
    display: flex;
    align-items: baseline;
    justify-content: space-between;
    margin-top: 1.5rem;
}

.shop-page-product-price .price{
    font-weight: bold;
}

.shop-page-product-btn{
    color: var(--dark);
    border: 1px solid var(--dark);
    background-color: white;
    border-radius: 50%;
    padding: 0.2rem 0.4rem;
    transition: all 0.3s ease;
}

.shop-page-product-btn:hover{
    color: white;
    border: 1px solid var(--blue);
    background-color: var(--blue);
}

</style>