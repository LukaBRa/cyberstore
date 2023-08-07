<script setup>

import Navbar from '../Layout/Navbar.vue';
import Footer from '../Layout/Footer.vue';
import Cart from '../Layout/Cart.vue';
import ProductAttribute from '../Components/ProductAttribute.vue';
import { ref } from 'vue';
 
const showCart = ref(false);

const toggleCart = () => {
    showCart.value = !showCart.value;
}

</script>

<template>

<div class="product-page">

    <Navbar @toggleCart="toggleCart"/>
    <Cart :displayCart="showCart" @closeCart="toggleCart"/>

    <div class="product-layout mt-5 mb-5">
        <div class="container">

            <div class="row justify-content-between">

                <div class="col-lg-7 col-12">

                    <div class="product-page-image">
                        <img src="/images/homepage/monitor-card.png" alt="Product">
                    </div>

                </div>

                <div class="col-lg-4 col-12">
                    <p class="product-page-product-name">LENOVO V15 G2 ITLi5 i5/8/256 82KB000SYA</p>
                    <div class="product-page-branding">
                        <p><span class="bold-accent">Model:</span> 82KB000SYA/8</p>
                        <p><span class="bold-accent">Brand:</span> Lenovo</p>
                    </div>
                    <p class="product-page-price"><span class="bold-accent">Price:</span> $1260</p>
                    <div class="product-page-quantity">
                        <button>-</button>
                        <p>4</p>
                        <button>+</button>
                    </div>
                    <button class="product-page-btn">Add to cart</button>
                </div>

            </div>

            <div class="product-page-description">
                <div class="attributes">
                        <ProductAttribute />
                        <ProductAttribute />
                        <ProductAttribute />
                        <ProductAttribute />
                        <ProductAttribute />
                </div>

                <div class="comments">
                    
                </div>

            </div>

        </div>
    </div>

    <Footer />

</div>

</template>

<style scoped>

.product-page-image img{
    width: 100%;
    height: 100%;
    object-fit: contain;
}

.product-page-description{
    border: 1px solid lightgray;
    padding: 0.5rem;
}

.product-page-product-name{
    font-size: 1.5rem;
    font-weight: bold;
}

.bold-accent{
    font-weight: bold;
}

.product-page-price{
    font-size: 1.3rem;
    margin-top: 2rem;
}

.product-page-quantity{
    display: flex;
    gap: 1rem;
    border: 1px solid lightgray;
    width: max-content;
    padding: 0.5rem 1rem;
    align-items: baseline;
    height: max-content;
    font-size: 1.2rem;
    border-radius: 30px;
    margin-bottom: 1rem;
    color: var(--dark);
}

.product-page-quantity button{
    border: none;
    background: none;
    font-size: 1.3rem;
    transition: all 0.3s ease;
    color: var(--dark);
    font-weight: bold;
}

.product-page-quantity button:hover{
    color: var(--blue);
}

.product-page-quantity p{
    margin: 0;
}

.product-page-btn{
    margin-top: 1rem;
    width: 100%;
    padding: 0.5rem;
    background-color: var(--blue);
    border: 1px solid var(--blue);
    color: white;
    transition: all 0.3s ease;   
}

.product-page-btn:hover{
    background-color: white;
    color: var(--dark);
    border: 1px solid var(--dark);
}

</style>