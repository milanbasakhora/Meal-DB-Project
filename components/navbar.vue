<template>
    <div class="sticky top-0">
        <section class="bg-green-600 shadow-lg">
            <nav>
                <div class="container mx-auto flex justify-between items-center p-4 font-semibold text-gray-100 text-xl h-16">
                    <div>
                        <nuxt-link to="/" class="text-2xl">Salmonday</nuxt-link>
                    </div>
                    <div class="flex items-baseline space-x-8 ">
                        <nuxt-link to="/" class="text-yellow-200 ">Home</nuxt-link>
                        <nuxt-link to="about" class="hover:text-yellow-200">About</nuxt-link>
                        <nuxt-link to="meals" class="hover:text-yellow-200">Meals</nuxt-link>
                        <nuxt-link to="pricing" class="hover:text-yellow-200">Pricing</nuxt-link>
                        <nuxt-link to="contact" class="hover:text-yellow-200">Contact</nuxt-link>
                    </div>
                </div>
            </nav>
        </section>
    </div>
</template>

<script setup>

</script>

<style lang="scss" scoped></style>