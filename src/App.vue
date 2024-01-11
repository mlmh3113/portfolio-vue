<script setup>
import NavComponent from './components/NavComponent.vue'
import HeroComponent from './components/HeroComponent.vue'
import AboutComponent from './components/AboutComponent.vue'
import PortfolioComponent from './components/PortfolioComponent.vue'
import ContactComponent from './components/ContactComponent.vue'
import FooterComponent from './components/FooterComponent.vue'

import { ref } from 'vue';


const dark = ref(true)


const darkMode = ()=>{
    dark.value = !dark.value
}


</script>

<template>

<NavComponent @darkMode="darkMode" :dark="dark"/>
<HeroComponent @darkMode="darkMode" :dark="dark" />
<AboutComponent @darkMode="darkMode" :dark="dark"/>
<PortfolioComponent @darkMode="darkMode" :dark="dark"/>
<ContactComponent @darkMode="darkMode" :dark="dark"/>
<FooterComponent @darkMode="darkMode" :dark="dark"/>

</template>

<style>

body {
    font-family: 'Onest', sans-serif;
    color: black;
    font-size: larger;
    
}

html {
    scroll-behavior: smooth;
    scroll-padding-top: 80px;
  }

.dark{
    color: aliceblue;
}

</style>


