<script setup>

import { ref } from 'vue';

const showNavbarSmall = ref(false);

const toggleNavbarSmall = () => {
    showNavbarSmall.value = !showNavbarSmall.value;
}

</script>

<template>

<nav>

    <div class="top-menu container">
        <a href="/" class="logo">
            CYBERSTORE<span class="blue-accent">.</span>
        </a>
        <div class="search-box d-sm-none d-none d-lg-block">
            <select>
                <option>All categories</option>
                <option>PC</option>
                <option>Monitor</option>
                <option>Graphic Card</option>
                <option>Processor</option>
                <option>Memory</option>
            </select>
            <input type="text" placeholder="Search for Product...">
            <a href="" class="search-btn"><i class="fa-solid fa-magnifying-glass fa-rotate-90"></i></a>
        </div>
        <div class="button-group d-sm-none d-none d-lg-flex">
            <a href=""><i class="fa-regular fa-user"></i></a>
            <a href=""><i class="fa-regular fa-heart"></i></a>
            <button @click="$emit('toggleCart')"><i class="fa-solid fa-cart-shopping"></i></button>
        </div>
        <button @click="toggleNavbarSmall" class="toggle-btn d-block d-lg-none"><i class="fa-solid fa-bars"></i></button>
    </div>

    <div class="bottom-menu d-sm-none d-none d-lg-block">
        <div class="bottom-menu-content container">
            <div class="bottom-menu-links">
                <a href="" class="bottom-menu-link">Home</a>
                <a href="" class="bottom-menu-link">Shop</a>
                <a href="" class="bottom-menu-link">About Us</a>
            </div>
            <div class="bottom-menu-phone">
                Call us: <a href="tel: +381866-540-3229" class="bottom-menu-link">(+381)866-540-3229</a>
            </div>
        </div>
    </div>

    <div class="nav-small d-lg-none" :class="{ 'active': showNavbarSmall }">
        <div>
            <div class="px-2 w-100 float-btn-end"><button @click="toggleNavbarSmall" class="close-sm-menu"><i class="fa-solid fa-xmark"></i></button></div>
            <div class="nav-small-links">
                <a href="">Home</a>
                <a href="">Shop</a>
                <a href="">About us</a>
            </div>
        </div>

        <div class="nav-small-button-group" >
            <div><a href="#"><i class="fa-regular fa-user"></i></a></div>
            <div><a href=""><i class="fa-solid fa-magnifying-glass fa-rotate-90"></i></a></div>
            <button @click="$emit('toggleCart')"><i class="fa-solid fa-cart-shopping"></i></button>
            <div><a href=""><i class="fa-regular fa-heart"></i></a></div>
        </div>
    </div>

</nav>

</template>

<style>

nav{
    position: relative;
}

:root{
    --dark: rgb(43, 43, 43);
    --blue: #3f68da;
    --light-gray: #eeeeee;
}

.top-menu{
    display: flex;
    align-items: center;
    justify-content: space-between;
    padding: 2rem 0rem;
    border-bottom: 1px solid var(--light-gray);
}

.logo{
    text-decoration: none;
    color: var(--dark);
    font-weight: bold;
    font-size: 2rem;
}

.blue-accent{
    color: var(--blue);
}

select{
    background-color: var(--light-gray);
    border: var(--light-gray);
    padding: 0.8rem 1rem;
    margin: 2px;
    margin-right: 20px;
}

.search-box{
    border: 1px solid var(--light-gray);
}

.search-box input{
    border: none;
    width: 20rem;
}

.search-box input:focus{
    outline: none;
}

.search-btn{
    background-color: var(--blue);
    color: white;
    padding: 1rem;
    margin-left: 20px;
}

.button-group{
    display: flex;
    align-items: center;
    gap: 1.5rem;
}

.button-group > * {
    color: var(--dark);
    background: none;
    border: none;
    font-size: 1.3rem;
}

.bottom-menu{
    background-color: var(--blue);
}

.bottom-menu-content{
    display: flex;
    align-items: center;
    justify-content: space-between;
    padding: 1rem 0rem;
    font-size: 1rem;
    font-weight: bold;
}

.bottom-menu-link{
    color: white;
    text-decoration: none;
    transition: all 0.3s ease;
}

.bottom-menu-link:hover{
    color: var(--light-gray);
}

.bottom-menu-links{
    display: flex;
    gap: 3rem;
}

.bottom-menu-phone{
    color: white;
}

.toggle-btn{
    display: none;
    background: none;
    border: none;
    font-size: 1.5rem;
    transition: all 0.3s ease;
}

.toggle-btn:hover{
    color: var(--blue);
}

.nav-small {
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
}

.nav-small.active{
    transform: translateX(0);
}

.float-btn-end{
    display: flex;
    justify-content: end;
}

.close-sm-menu{
    background: none;
    border: none;
    font-size: 1.5rem;
    padding: 0.5rem;
}

.nav-small-links{
    display: flex;
    flex-direction: column;
}

.nav-small-links > a {
    padding: 1rem;
    text-decoration: none;
    color: var(--dark);
    font-weight: bold;
    transition: all 0.3s ease;
    font-size: 1.3rem;
}

.nav-small-links > a:hover{
    background-color: var(--light-gray);
}

.nav-small-button-group{
    height: 5%;
    display: flex;
}

.nav-small-button-group > *{
    background: none;
    border: 1px solid var(--light-gray);
    width: 25%;
    font-size: 1.2rem;
}

.nav-small-button-group > div{
    position: relative;
}

.nav-small-button-group a{
    position: absolute;
    color: var(--dark);
    width: 100%;
    height: 100%;
    display: flex;
    align-items: center;
    justify-content: center;
    transition: all 0.3s ease;
}

.nav-small-button-group a:hover{
    background-color: var(--light-gray);
}

.nav-small-button-group button{
    transition: all 0.3s ease;
}

.nav-small-button-group button:hover{
    cursor: pointer;
    background-color: var(--light-gray);
}

</style>