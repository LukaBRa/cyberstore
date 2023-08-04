<script setup>

import { ref, onMounted } from 'vue';
import CarouselItem from '../Components/CarouselItem.vue';

const carouselItems = [
    {
        id: 1,
        firstTitle: "It's PowerFull",
        secondTitle: "It's CyberStore",
        description: 'Lorem ipsum dolor, sit amet consectetur adipisicing elit. Expedita tenetur quod et temporibus a, soluta cum deserunt unde alias perferendis eaque dolore. Veniam, atque hic quisquam ipsa dicta maxime dolore.',
        imageUrl: '/images/homepage/pc-carousel.png'
    },
    {
        id: 2,
        firstTitle: "Cutting Edge",
        secondTitle: "Technology Store",
        description: 'Lorem ipsum dolor, sit amet consectetur adipisicing elit. Expedita tenetur quod et temporibus a, soluta cum deserunt unde alias perferendis eaque dolore. Veniam, atque hic quisquam ipsa dicta maxime dolore.',
        imageUrl: '/images/homepage/monitor-carousel.png'
    },
    {
        id: 3,
        firstTitle: "Modern and",
        secondTitle: "Just Captivating",
        description: 'Lorem ipsum dolor, sit amet consectetur adipisicing elit. Expedita tenetur quod et temporibus a, soluta cum deserunt unde alias perferendis eaque dolore. Veniam, atque hic quisquam ipsa dicta maxime dolore.',
        imageUrl: '/images/homepage/components-carousel.png'
    }
];

const currentItem = ref(0);

const swipeLeft = () => {
    if(currentItem.value == 0){
        currentItem.value = carouselItems.length - 1;
    }else{
        currentItem.value--;
    }
}

const swipeRight = () => {
    if(currentItem.value == carouselItems.length - 1){
        currentItem.value = 0;
    }else{
        currentItem.value++;
    }
}


</script>

<template>

<div class="carousel d-none d-lg-block">

    <div class="switches">
        <button @click="swipeLeft" class="carousel-switch-btn"><i class="fa-solid fa-chevron-left"></i></button>
        <button @click="swipeRight" class="carousel-switch-btn"><i class="fa-solid fa-angle-right"></i></button>
    </div>

    <CarouselItem :key="carouselItems[currentItem].id" :item="carouselItems[currentItem]"/>
    
</div>

</template>

<style>

:root{
    --dark: rgb(43, 43, 43);
    --blue: #3f68da;
    --light-gray: #eeeeee;
}

.carousel{
    background-color: var(--light-gray);
    width: 100vw;
    height: 40vh;
    position: relative;
}

.switches{
    position: absolute;
    display: flex;
    justify-content: space-between;
    width: 100%;
    top: 50%;
}

.carousel-switch-btn{
    margin-left: 1.5rem;
    margin-right: 1.5rem;
    border: none;
    background-color: white;
    padding: 0.5rem 1rem;
    border-radius: 50%;
    font-size: 1.5rem;
    transition: all 0.3s ease;
    box-shadow: rgba(149, 157, 165, 0.2) 0px 8px 24px;
}

.carousel-switch-btn:hover{
    color: var(--blue);
}

</style>