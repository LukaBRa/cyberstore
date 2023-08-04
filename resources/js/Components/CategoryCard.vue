<script setup>

const props = defineProps(['title', 'imageUrl', 'color']);

</script>

<template>

<div class="category-card" :style="{ backgroundColor: color }">
    <div class="category-card-text">
        <h4 class="m-3">{{ title }}</h4>
        <a href="" class="item-link m-3">Shop Now</a>
    </div>
    <div class="category-card-image">
        <img :src="imageUrl" alt="Category" class="img-fluid"/>
    </div>
</div>

</template>

<style>

.category-card{
    display: flex;
    align-items: center;
    height: 10rem;
    width: 30%;
}

.category-card-image{
    height: 100%;
    width: 100%;
}

.category-card-image > img{
    height: 100%;
    width: 100%;
    object-fit: contain;
}

@media only screen and (max-width: 768px) {
    .category-card{
    display: flex;
    align-items: center;
    height: 10rem;
    width: 100%;
}
}



</style>