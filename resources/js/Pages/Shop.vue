<script setup>

import Navbar from '../Layout/Navbar.vue';
import Footer from '../Layout/Footer.vue';
import Cart from '../Layout/Cart.vue';
import ShopPage from '../Layout/ShopPage.vue';
import { ref } from 'vue';

const showCart = ref(false);

const toggleCart = () => {
    showCart.value = !showCart.value;
}

</script>

<template>

<div>

    <Navbar @toggleCart="toggleCart"/>
    <Cart :displayCart="showCart" @closeCart="toggleCart"/>

    <div class="container">
        <ShopPage />
    </div>

    <Footer />

</div>

</template>

<style scoped>



</style>