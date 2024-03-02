<script setup>
import Navbar from '../components/Navbar.vue'
import Banner from '../components/Banner.vue'

</script>

<template>

    <div>
        <header>
            <Navbar/>
            <Banner/>
        </header>
        <slot/>
    </div>

</template>