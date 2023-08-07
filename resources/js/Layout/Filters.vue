<script setup>



</script>

<template>

<div class="filter-list">

    <div class="filter">
        <p class="filter-name">Brand</p>
        <div class="checkbox-group">
            <div class="checkbox-wrapper"><input type="checkbox" name="" id="">Asus</div>
            <div class="checkbox-wrapper"><input type="checkbox" name="" id="">Asus</div>
            <div class="checkbox-wrapper"><input type="checkbox" name="" id="">Asus</div>
            <div class="checkbox-wrapper"><input type="checkbox" name="" id="">Asus</div>
            <div class="checkbox-wrapper"><input type="checkbox" name="" id="">Asus</div>
        </div>
    </div>

    <div class="filter">
        <p class="filter-name">Resolution</p>
        <div class="checkbox-group">
            <div class="checkbox-wrapper"><input type="checkbox" name="" id="">Asus</div>
            <div class="checkbox-wrapper"><input type="checkbox" name="" id="">Asus</div>
            <div class="checkbox-wrapper"><input type="checkbox" name="" id="">Asus</div>
            <div class="checkbox-wrapper"><input type="checkbox" name="" id="">Asus</div>
            <div class="checkbox-wrapper"><input type="checkbox" name="" id="">Asus</div>
        </div>
    </div>

    <div class="filter">
        <p class="filter-name">Screen Diagonal </p>
        <div class="checkbox-group">
            <div class="checkbox-wrapper"><input type="checkbox" name="" id="">Asus</div>
            <div class="checkbox-wrapper"><input type="checkbox" name="" id="">Asus</div>
            <div class="checkbox-wrapper"><input type="checkbox" name="" id="">Asus</div>
            <div class="checkbox-wrapper"><input type="checkbox" name="" id="">Asus</div>
            <div class="checkbox-wrapper"><input type="checkbox" name="" id="">Asus</div>
        </div>
    </div>
</div>

</template>

<style scoped>

.filter{
    margin-bottom: 1rem;
}
.filter-list{
    border: 1px solid var(--light-gray);
    padding: 0.5rem;
}

.filter-name{
    font-weight: bold;
}

.checkbox-group{
    display: flex;
    flex-direction: column;
    margin-left: 0.5rem;
}

.checkbox-wrapper{
    display: flex;
    align-items: baseline;
    gap: 0.5rem;
}

</style>