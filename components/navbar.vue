<template>
    <div class="sticky top-0 z-50">
        <section class="bg-green-600 shadow-lg bg-opacity-90 backdrop-blur-sm">
            <nav>
                <div class="container mx-auto flex justify-between items-center p-4 font-semibold text-gray-100 text-xl h-16">
                    <div>
                        <nuxt-link to="/" active-class="logo" class="text-2xl">Salamandish 🥗</nuxt-link>
                    </div>
                    <div class="flex items-center gap-8 max-sm:hidden">
                        <nuxt-link to="/" class="hover:text-yellow-200">Home</nuxt-link>
                        <nuxt-link to="/about" class="hover:text-yellow-200">About</nuxt-link>
                        <nuxt-link to="/meals" class="hover:text-yellow-200">Meals</nuxt-link>
                        <nuxt-link to="/pricing" class="hover:text-yellow-200">Pricing</nuxt-link>
                        <nuxt-link to="/contact" class="hover:text-yellow-200">Contact</nuxt-link>
                    </div>
                </div>
            </nav>
        </section>
    </div>
</template>

<script setup>

</script>

<style>
.router-link-active{
    color: rgb(254 240 138 / var(--tw-text-opacity));
}
</style>