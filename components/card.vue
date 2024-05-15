<template>
    <div class="bg-green-100 h-[440px] rounded-md w-full shadow-lg overflow-hidden hover:shadow-xl cursor-pointer" @click="navigateTo(`/meals/${monkey.idMeal}`)">
        <div>
            <img :src="monkey.strMealThumb" alt="yo" loading="lazy">
        </div>

        <div class="p-4">
            <h3 class="text-3xl font-bold">{{ monkey.strMeal }}</h3>
            <nuxt-link to="">Details</nuxt-link>
        </div>
    </div>
</template>

<script setup>
defineProps(["monkey"]);
</script>

<style lang="scss" scoped></style>