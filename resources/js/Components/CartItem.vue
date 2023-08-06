<script setup>



</script>

<template>

<div class="cart-item">
    <div class="cart-item-img">
        <img src="/images/homepage/keyboard-card.png" alt="Product image">
    </div>
    <div class="cart-item-info">
        <p class="cart-item-name">LOGITECH K400 PLUS WIRELESS TOUCH YU-SRB 920-007119</p>
        <div class="cart-item-price">
            <p>$59</p>
            <div class="cart-item-btn-group">
                <button>-</button>
                <p>4</p>
                <button>+</button>
            </div>
        </div>
    </div>
</div>

</template>

<style>

.cart-item{
    display: flex;
    align-items: center;
    border-bottom: 1px solid rgb(231, 231, 231);
    padding-top: 0.5rem;
}

.cart-item-name{
    font-weight: bold;
}

.cart-item-img{
    width: 300px;
    height: 100px;
}

.cart-item-price{
    display: flex;
    align-items: center;
    justify-content: space-between;
    font-size: 1.2rem;
}

.cart-item-img img{
    width: 100%;
    height: 100%;
}

.cart-item-btn-group{
    display: flex;
    gap: 1rem;
    align-items: baseline;
}

.cart-item-btn-group button{
    background: none;
    border: none;
    color: var(--dark);
    transition: all 0.3s ease;
    font-size: 1.5rem;
}

.cart-item-btn-group button:hover{
    color: var(--blue);
}

</style>