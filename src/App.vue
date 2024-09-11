<script setup lang="ts">
import NavBar from './components/Navigation/NavBar.vue';
import Main from './components/main/main.vue';
import About from './components/About/About.vue';
import Feature from './components/Feature/Feature.vue';
import Team from './components/Team/Team.vue';
import ContactUs from './components/Footer/ContactUs.vue';
import Demo from './components/Demo/Demo.vue';
import Footer from './components/Footer/Footer.vue';
</script>

<template>
  <NavBar/>
  <div class="meat">
    <Main/>
    <About/>
    <Feature/>
    <Demo />
    <Team/>
    <ContactUs/>
  </div>
  <Footer/>
</template>

<style scoped>
.meat {
  display: flex;
  flex-direction:column;
  justify-content: space-between;
  align-items: center;
    padding: 0em;
    margin-top: 0;
    margin-bottom: 0;
    width: 100vw;
}
</style>
