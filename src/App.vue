<script setup lang="ts">
import NavBar from './components/Navigation/NavBar.vue'
import Main from './main/main.vue'
import HelloWorld from './components/HelloWorld.vue'
import About from './components/About/About.vue'
import Feature from './components/Feature/Feature.vue'
import Team from './components/TeamMembers/collaborators.vue'
import ContactUs from './components/Footer/ContactUs.vue'
import Footer from "./components/Footer/Footer.vue"
</script>

<template>
  <NavBar/>
  <Main/>
  <HelloWorld msg="Vite + Vue" />
  <About/>
  <Team/>
  <ContactUs/>
  <Footer/>
</template>

<style scoped>

</style>
