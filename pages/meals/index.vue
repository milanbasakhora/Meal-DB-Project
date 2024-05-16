<template>
    <div class="container mx-auto py-4">
        <div class="text-center mb-4">
            <p class="py-4 font-bold text-xl text-green-800">Search Meals</p>
            <input placeholder="Type in any keyword" class="w-1/2 border px-4 py-2 border-green-300 outline-none rounded-md focus:border-green-400 shadow-sm" @keyup="searchMeals(searchKeyword)" v-model="searchKeyword">
        </div>
        <div class="grid grid-cols-4 gap-8 py-4">
            <div v-for="meal in beefs.meals" :key="meal.idMeal">
                <card :monkey="meal" />
            </div>
        </div>
    </div>
</template>

<script setup>
const searchKeyword = ref(``)
const url = ref(`https://www.themealdb.com/api/json/v1/1/search.php?s=a`);
const { data: beefs } = await useFetch(url);

function searchMeals(naruto) {
    url.value = `https://www.themealdb.com/api/json/v1/1/search.php?s=${naruto}`;
}
</script>

<style lang="scss" scoped></style>