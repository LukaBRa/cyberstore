<script setup>

const props = defineProps(['item']);

</script>

<template>

<div class="carousel-item-section container">
        <div class="carousel-column">
            <h1>{{ item.firstTitle }}</h1>
            <h1 class="mb-4">{{ item.secondTitle.split(' ')[0] }} <span class="bold-accent">{{ item.secondTitle.split(' ')[1] }}</span></h1>
            <p class="mb-4">{{ item.description }}</p>
            <a href="" class="item-link">Shop Now</a>
        </div>
        <div class="carousel-column image-column">
            <img :src="item.imageUrl" alt="CyberStore Promotion">
        </div>
</div>

</template>

<style>

:root{
    --dark: rgb(43, 43, 43);
    --blue: #3f68da;
    --light-gray: #eeeeee;
}

.carousel-item-section{
    height: 100%;
    display: flex;
    align-items: center;
}

.carousel-column{
    width: 50%;
    height: 100%;
    display: flex;
    flex-direction: column;
    justify-content: center;
}

.carousel-column h1{
    animation: titleEntrance 1s ease 0s 1 normal forwards;
}

.carousel-column p{
    animation: paragraphEntrance 2s ease 0s 1 normal forwards;
}

.carousel-column a{
    animation: paragraphEntrance 2s ease 0s 1 normal forwards;
}

.image-column{
    display: flex;
    align-items: center;
    justify-content: center;
}

.image-column img{
    width: 50%;
    animation: imageEntrance 2s ease 0s 1 normal forwards;
}

.bold-accent{
    font-weight: bold;
}

@keyframes imageEntrance {
	0% {
		opacity: 0;
	}

	100% {
		opacity: 1;
	}
}

@keyframes titleEntrance {
	0% {
		opacity: 0;
		transform: translateX(50px);
	}

	100% {
		opacity: 1;
		transform: translateX(0);
	}
}

@keyframes paragraphEntrance {
	0% {
		opacity: 0;
		transform: translateX(50px);
	}

	100% {
		opacity: 1;
		transform: translateX(0);
	}
}


</style>