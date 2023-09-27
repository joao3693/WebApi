<script setup>
const drink = defineProps(["name","baseUrlSvg"])
</script>

<template>
    <div class="col-4">
        <div class="card p-2 mb-3">
            <p class="text-center">{{strDrink.name}}</p>
            <img
            :src="baseUrlSvg" class="card-img-top"
            alt="..."
            height="80"
            />
        </div>
    </div>
    
</template>

<style>

</style>