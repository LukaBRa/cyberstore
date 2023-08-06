<script setup>

import Navbar from '../Layout/Navbar.vue';
import Carousel from '../Layout/Carousel.vue';
import CategoryCard from '../Components/CategoryCard.vue';
import HomeProductCard from '../Components/HomeProductCard.vue';
import Footer from '../Layout/Footer.vue';
import Cart from '../Layout/Cart.vue';
import { ref } from 'vue';

const products = [
    {
        id: 1,
        category: 'Laptop & Tablet',
        rating: 5,
        name: 'Apple MacBook Pro With Touch Bar MF841DSN/A 13"',
        price: 1267,
    },
    {
        id: 2,
        category: 'Laptop & Tablet',
        rating: 5,
        name: 'Apple MacBook Pro With Touch Bar MF841DSN/A 13"',
        price: 1267,
    },
    {
        id: 3,
        category: 'Laptop & Tablet',
        rating: 5,
        name: 'Apple MacBook Pro With Touch Bar MF841DSN/A 13"',
        price: 1267,
    },
    {
        id: 4,
        category: 'Laptop & Tablet',
        rating: 5,
        name: 'Apple MacBook Pro With Touch Bar MF841DSN/A 13"',
        price: 1267,
    },
    {
        id: 5,
        category: 'Laptop & Tablet',
        rating: 5,
        name: 'Apple MacBook Pro With Touch Bar MF841DSN/A 13"',
        price: 1267,
    },
    {
        id: 6,
        category: 'Laptop & Tablet',
        rating: 5,
        name: 'Apple MacBook Pro With Touch Bar MF841DSN/A 13"',
        price: 1267,
    }
];

const showCart = ref(false);

const toggleCart = () => {
    showCart.value = !showCart.value;
}

</script>

<template>

<div>

    <Navbar @toggleCart="toggleCart"/>
    <Carousel />
    <Cart :displayCart="showCart" @closeCart="toggleCart"/>

    <div class="container">
        <div class="category-cards">

            <CategoryCard title="Mobiles & Tablets" imageUrl="/images/homepage/iphone-card.png" color="#f3fcf1"/>
            <CategoryCard title="Computer Parts" imageUrl="/images/homepage/keyboard-card.png" color="#eeeeee"/>
            <CategoryCard title="Computers & Laptop" imageUrl="/images/homepage/monitor-card.png" color="#fdf1f7"/>

        </div>
    </div>

    <div class="container margin-top-5">
        <h3 class="sub-title mb-4">Recently added</h3>

        <div class="row mb-5 gy-4">
            <HomeProductCard v-for="product in products" :key="product.id" :product="product" />
        </div>

    </div>

    <div class="container sponsors">
        <div class="sponsor border-right">
            <img src="/images/homepage/apple.png" alt="Apple">
        </div>
        <div class="sponsor border-right">
            <img src="/images/homepage/asus.png" alt="Asus">
        </div>
        <div class="sponsor border-right">
            <img src="/images/homepage/ibm.png" alt="IBM">
        </div>
        <div class="sponsor border-right">
            <img src="/images/homepage/intel.png" alt="Intel">
        </div>
        <div class="sponsor border-right">
            <img src="/images/homepage/nvidia.png" alt="Nvidia">
        </div>
        <div class="sponsor">
            <img src="/images/homepage/samsung.png" alt="Samsung">
        </div>
    </div>

    <div class="container-fluid parallax-bg margin-bottom-5">
        <div class="container parallax-container">
            <div class="parallax-div">
                <div class="parallax-div-head">
                    <button class="parallax-div-save-btn"><i class="fa-regular fa-heart"></i></button>
                </div>
                <div class="parallax-product">
                    <div class="parallax-product-image">
                        <img src="/images/homepage/components-carousel.png" alt="Processor">
                    </div>
                    <div class="parallax-product-info">
                        <p class="parallax-product-category">Processor</p>
                        <a href="" class="parallax-product-name">AMD Ryzen 7 7700 3.8GHz (5.3GHz) Procesor</a>
                        <div class="parallax-product-price">
                            <p class="price">$200</p>
                            <button><i class="fa-solid fa-cart-plus"></i></button>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>

    <div class="container mb-5">
        <div class="discount-div row">
            <div class="discount-info col-12 col-lg-6">
                <h1>Save Up to 40% Off</h1>
                <p>On All Apple Products</p>
                <a href="" class="discount-link mt-5">Shop Now</a>
            </div>
            <div class="discount-image col-12 col-lg-6">
                <img src="/images/homepage/apple-products.png" alt="Apple Products">
            </div>
        </div>
    </div>

    <Footer />

</div>

</template>

<style>

.category-cards{
    display: flex;
    justify-content: space-between;
    align-items: center;
    margin: 5rem 0rem;
}

.sponsors{
    background-color: var(--light-gray);
    padding: 1rem;
    border-radius: 20px;
    display: flex;
    margin-bottom: 2rem;
    margin-top: 5rem;
}

.sponsor{
    display: flex;
    align-items: center;
}

.border-right{
    border-right: 1px solid rgb(224, 224, 224);
}


.sponsor img{
    height: 50%;
    width: 100%;
    object-fit: contain;
}

.parallax-bg{
    background: linear-gradient( rgba(0, 0, 0, 0.5), rgba(0, 0, 0, 0.5) ), url('/images/homepage/parallax.jpg');
    background-repeat: no-repeat;
    background-size: cover;
    background-attachment: fixed;
    background-position: center;
    height: 45vh;
    margin-top: 5rem;
}

.parallax-container{
    height: 100%;
    display: flex;
    align-items: center;
}

.parallax-div{
    background-color: white;
    width: max-content;
    padding: 2rem;
    width: 60%;
}

.parallax-div-head{
    display: flex;
    justify-content: end;
}

.parallax-div-save-btn{
    background: none;
    border: none;
    font-size: 1.4rem;
    color: lightgrey;
    transition: all 0.3s ease;
}

.parallax-div-save-btn:hover{
    color: var(--blue);
}

.parallax-product{
    display: flex;
    align-items: center;
    gap: 1rem;
}

.parallax-product-category{
    color: rgb(182, 182, 182);
}

.parallax-product-name{
    color: var(--dark);
    font-size: 1.2rem;
    font-weight: bold;
    text-decoration: none;
    transition: all 0.3s ease;
}

.parallax-product-name:hover{
    text-decoration: underline;
}

.parallax-product-price{
    display: flex;
    align-items: baseline;
    justify-content: space-between;
    margin-top: 1.5rem;
}

.parallax-product-price .price{
    color: var(--blue);
    font-weight: bold;
}

.parallax-product-price button{
    background-color: white;
    font-size: 1.2rem;
    border: 1px solid var(--dark);
    border-radius: 50%;
    padding: 0.3rem 0.4rem;
    transition: all 0.3s ease;
    color: var(--dark);
}

.parallax-product-price button:hover{
    color: white;
    background-color: var(--blue);
    border: 1px solid var(--blue);
}

.discount-div{
    background-color: var(--dark);
    padding: 1rem 2rem;
    display: flex;
    align-items: center;
    justify-content: space-between;
}

.discount-info{
    color: white;
    height: 20vh;
    display: flex;
    flex-direction: column;
    justify-content: center;
}

.discount-info h1{
    font-weight: bold;
}

.discount-info p{
    font-size: 1.1rem;
}

.discount-image{
    display: flex;
    align-items: center;
    justify-content: center;
}

.discount-image img{
    height: 100%;
    width: 50%;
    object-fit: contain;
}

.discount-link{
    background-color: var(--blue);
    color: white;
    width: max-content;
    padding: 0.7rem 1.5rem;
    border-radius: 30px;
    text-decoration: none;
    background: rgb(24,45,101);
    background: linear-gradient(49deg, rgba(24,45,101,1) 0%, rgba(67,110,230,1) 64%, rgba(0,212,255,1) 100%);
}

.discount-link:hover{
    animation-name: link-animation;
    animation-duration: 0.15s;
    animation-timing-function: ease-in;
    animation-delay: 0s;
    animation-fill-mode: both;
}

@media only screen and (max-width: 768px) {
    .category-cards{
    display: flex;
    flex-direction: column;
    gap: 2rem;
    justify-content: space-between;
    align-items: center;
    margin: 3rem 0rem;
    }
}

@keyframes link-animation{
    0% {background: rgb(24,45,101);
    background: linear-gradient(49deg, rgba(24,45,101,1) 0%, rgba(67,110,230,1) 64%, rgba(0,212,255,1) 100%);}
    25% {background: rgb(24,45,101);
    background: linear-gradient(106deg, rgba(24,45,101,1) 0%, rgba(67,110,230,1) 64%, rgba(0,212,255,1) 100%);}
    50% {background: rgb(24,45,101);
    background: linear-gradient(210deg, rgba(24,45,101,1) 0%, rgba(67,110,230,1) 64%, rgba(0,212,255,1) 100%);}
    /* 75% {
        background: rgb(24,45,101);
        background: linear-gradient(150deg, rgba(24, 45, 101, 1) 0%, rgba(67, 110, 230, 1) 64%, rgba(0, 212, 255, 1) 100%);
    } */
    100% {background: rgb(24,45,101);
    background: linear-gradient(320deg, rgba(24,45,101,1) 0%, rgba(67,110,230,1) 64%, rgba(0,212,255,1) 100%);}
}


</style>