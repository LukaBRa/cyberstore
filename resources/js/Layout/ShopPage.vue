<script setup>

import Filters from '../Layout/Filters.vue';
import ShopPageProduct from '../Components/ShopPageProduct.vue';

</script>

<template>

<div class="shop-page">
    <div class="shop-page-header">
        <h3>Monitors</h3>
        <select>
            <option>Sort by</option>
            <option>Price ascending</option>
            <option>Price descending</option>
            <option>Rating</option>
        </select>
    </div>

    <div class="shop-page-content">
        <div class="row">
            <!-- Filters Component -->
            <div class="col-lg-3">
                <Filters />
            </div>

            <!-- Products list (Product component) -->
            <div class="col-lg-9 col-12">
                <div class="container">
                    <div class="row justify-content-evenly g-3">
                        <ShopPageProduct />
                        <ShopPageProduct />
                        <ShopPageProduct />
                        <ShopPageProduct />
                        <ShopPageProduct />
                        <ShopPageProduct />
                        <ShopPageProduct />
                        <ShopPageProduct />
                        <ShopPageProduct />
                    </div>
                </div>
            </div>

        </div>
    </div>

</div>

</template>

<style scoped>

.shop-page-header{
    display: flex;
    align-items: flex-end;
    justify-content: space-between;
    margin: 2rem 0rem;
    padding-bottom: 1rem;
    border-bottom: 1px solid var(--light-gray);
}


</style>