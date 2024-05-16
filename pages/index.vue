<template>
    <div>
        <!-- Hero Section -->
        <section>
            <div class="container mx-auto grid grid-cols-2 gap-5 max-sm:gap-0 max-sm:grid-cols-1 max-sm:text-center max-sm:pb-8">
                <div class="px-4 flex justify-center items-center p-10">
                    <div class="border-8 border-green-500 rounded-full">
                        <div class="bg-green-100 h-[500px] w-[500px] rounded-full bg-opacity-10 backdrop-blur-3xl max-sm:h-[300px] max-sm:w-[300px]">
                            <img class="h-[500px] w-[500px] object-cover max-sm:h-[300px] max-sm:w-[300px]" src="https://www.themealdb.com/images/ingredients/Salmon.png" alt="">
                        </div>
                    </div>
                </div>
                <div class="flex justify-center items-center max-sm:px-10">
                    <div class="flex flex-col gap-5">
                        <h1 class="text-6xl font-bold italic max-sm:text-4xl">Salmon Silimonical Super Sals</h1>
                        <p class="max-sm:text-smx">Lorem ipsum dolor sit amet consectetur adipisicing elit. Asperiores,
                            aliquid? Vel quo rerum
                            quidem natus officiis? Vel, explicabo obcaecati praesentium cumque voluptatem quas dolorum
                            optio officia commodi atque ad consequatur?</p>
                        <div>
                            <button type="button"
                                class="text-white bg-green-700 hover:bg-green-800 rounded-lg px-4 py-2 me-2 mx-1 mb-2 font-medium" @click="navigateTo('#meals')">Let's
                                Eat</button>
                        </div>
                    </div>
                </div>
            </div>
        </section>
        <!-- Hero Section End -->

        <!-- About Section -->
        <section class="bg-green-100 py-8">
            <div class="container mx-auto grid grid-cols-2 gap-x-8 ">
                <div class="flex justify-center items-center px-10">
                    <div class="">
                        <h1 class="text-5xl font-bold pb-6">About Us</h1>
                        <p class="pb-6 px-1">Lorem ipsum dolor sit amet consectetur adipisicing elit. Asperiores,
                            aliquid? Vel quo rerum
                            quidem natus officiis? Vel, explicabo obcaecati praesentium cumque voluptatem quas dolorum
                            optio officia commodi atque ad consequatur? Lorem ipsum dolor sit amet consectetur,
                            adipisicing elit. Velit eaque quam placeat quisquam, amet nostrum officiis assumenda sit
                            voluptates necessitatibus debitis, magnam veritatis id. Lorem ipsum dolor sit amet
                            consectetur adipisicing elit. Nisi fuga itaque quidem dolor suscipit officiis non tempora,
                            ex quam aperiam.</p>
                        <button type="button"
                            class="text-white bg-green-700 hover:bg-green-800 rounded-lg px-5 py-2.5 me-2 mx-1 mb-2 font-medium text-sm">Read
                            More</button>
                    </div>
                </div>
                <div class="px-4">
                    <img src="/images/dish.png" alt="">
                </div>
            </div>
        </section>
        <!-- About Section End -->

        <!-- Meals -->
        <section class="py-10" id="meals">
            <div class="meals container mx-auto space-y-8">
                <div>
                    <p>Choose Category</p>
                    <select class="w-full h-8 border border-green-300 outline-none" v-model="selectedCategory"
                        @change="changeUrl(selectedCategory)">
                        <option :value="category.strCategory" v-for="category in categorydata.categories"
                            :key="category.idCategory">{{
                                category.strCategory }}</option>
                    </select>
                </div>
                <div class="grid grid-cols-4 gap-8">
                    <div v-for="meal in donkey.meals" :key="meal.idMeal">
                        <card :monkey="meal" />
                    </div>
                </div>
            </div>
        </section>
        <!-- Meals End -->
    </div>
</template>

<script setup>
const selectedCategory = ref(`Beef`);
const url = ref(`https://www.themealdb.com/api/json/v1/1/filter.php?c=Starter`);
const { data: donkey } = await useFetch(url);
const { data: categorydata } = await useFetch('https://www.themealdb.com/api/json/v1/1/categories.php');
function changeUrl(selectedCategory) {
    url.value = `https://www.themealdb.com/api/json/v1/1/filter.php?c=${selectedCategory}`;
}
</script>

<style lang="scss" scoped></style>