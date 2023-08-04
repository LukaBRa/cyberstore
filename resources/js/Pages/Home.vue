<script setup>

import Navbar from '../Layout/Navbar.vue';
import Carousel from '../Layout/Carousel.vue';
import CategoryCard from '../Components/CategoryCard.vue';
import HomeProductCard from '../Components/HomeProductCard.vue';

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
]

</script>

<template>

<div>

    <Navbar />
    <Carousel />

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
        <div class="container">
            <div class="parallax-div">
                <HomeProductCard :key="products[0].id" :product="products[0]" />
            </div>
        </div>
    </div>

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
    background-image: url('/images/homepage/parallax.jpg');
    background-repeat: no-repeat;
    background-size: cover;
    background-attachment: fixed;
    background-position: center;
    height: 40vh;
    margin-top: 5rem;
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


</style>