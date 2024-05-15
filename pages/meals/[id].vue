<template>
    <div>
        <div class="contaner mx-auto px-20 py-20 bg-slate-100">
            <h1 class="text-4xl font-bold text-green-800 mb-10">😋 {{ meal.meals[0].strMeal }}</h1>
            <div class="grid gap-16 grid-cols-2">
                <div class="shadow-2xl rounded-2xl overflow-hidden border-4 border-green-500">
                    <img src="https://www.themealdb.com/images/media/meals/wvpsxx1468256321.jpg" alt="">
                </div>
                <div class="bg-green-100 p-10 rounded-2xl shadow-sm">
                    <h1><b>Category:</b> {{ meal.meals[0].strCategory }}</h1>
                    <h2><b>Area:</b> {{ meal.meals[0].strArea }}</h2>
                    <p><b>Instructions:</b> {{ meal.meals[0].strInstructions }}</p>
                </div>
            </div>
        </div>
    </div>
</template>

<script setup>
const {id} = useRoute().params
const {data:meal} = await useFetch(`https://www.themealdb.com/api/json/v1/1/lookup.php?i=${id}`)
</script>

<style lang="scss" scoped></style>