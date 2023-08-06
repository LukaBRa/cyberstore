<script setup>

import CartItem from '../Components/CartItem.vue';

const props = defineProps(['displayCart']);

</script>

<template>

<div class="cart" :class="{ 'active': displayCart }">

    <div class="title-items">
        <div class="cart-head">
            <button @click="$emit('closeCart')" class="close-cart-btn"><i class="fa-solid fa-chevron-right"></i></button>
        </div>
        <h2>Your Cart</h2>
        <div class="cart-items">
            <CartItem />
            <CartItem />
        </div>
    </div>

    <div class="cart-total">
        <p class="total">Total: $1450</p>
        <a href="" class="checkout-link">Checkout</a>
    </div>

</div>

</template>

<style>

.cart{
    position: fixed;
    display: flex;
    flex-direction: column;
    justify-content: space-between;
    top: 0;
    right: 0;
    transform: translateX(100%);
    height: 100vh;
    width: 350px;
    background-color: white;
    border-left: 1px solid var(--light-gray);
    transition: all 0.3s ease;
    padding: 0.5rem;
    overflow: auto;
}


h2{
    text-align: center;
    border-bottom: 1px solid rgb(231, 231, 231);
    padding: 1rem 0rem;
}

.cart.active{
    transform: translateX(0);
}

.cart-head{
    padding-bottom: 0.5rem;
}

.close-cart-btn{
    background: none;
    border: none;
    font-size: 1.2rem;
    color: var(--dark);
    transition: all 0.3s ease;
}

.close-cart-btn:hover{
    color: var(--blue);
}


.cart-total{
    width: 100%;
    border-top: 1px solid rgb(231, 231, 231);
    padding: 0.5rem 0rem;
}

.checkout-link{
    display: block;
    border: 1px solid var(--dark);
    width: 100%;
    padding: 0.5rem;
    text-decoration: none;
    text-align: center;
    color: var(--dark);
    font-size: 1.2rem;
    transition: all 0.3s ease;
}

.checkout-link:hover{
    background-color: var(--blue);
    color: white;
    border: 1px solid var(--blue);
}

.total{
    font-size: 1.2rem;
    font-weight: bold;
}


</style>