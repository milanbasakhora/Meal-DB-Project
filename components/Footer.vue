<template>
    <section class="bg-green-600">
        <div class="container mx-auto flex gap-4 justify-between text-white py-8">
            <nuxt-link to="/" class="text-2xl">Salmonday 🥗</nuxt-link>
            <p class="text-xl">@ {{ date }}, All Rights Reserved!</p>
            <p class="text-xl">Made with ❤️ by Salim</p>
        </div>
    </section>
</template>

<script setup>
const date = new Date().getFullYear()
</script>

<style lang="scss" scoped></style>