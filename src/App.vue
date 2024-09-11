<script setup lang="ts">
import NavBar from './components/Navigation/NavBar.vue';
import Main from './components/main/main.vue';
import About from './components/About/About.vue';
import Feature from './components/Feature/Feature.vue';
import Team from './components/Team/Team.vue';
import ContactUs from './components/Footer/ContactUs.vue';
import Footer from './components/Footer/Footer.vue';
</script>

<template>
  <NavBar/>
  <div class="meat">
    <Main/>
    <About/>
    <Feature/>
    <Team/>
    <ContactUs/>
  </div>
  <Footer/>
</template>

<style scoped>
.meat {
    padding: 0em;
    background: linear-gradient(to bottom, #131313 0%, #242424 100%);
    margin-top: 0;
    margin-bottom: 0;
    width: 100vw;
    box-sizing: border-box;
}

  .temp {
    margin: 10em 1em;
    border: .5em solid;
    border-radius: 2em;
    padding: 2em;

    display: flex;
    flex-wrap:wrap;
    /* justify-content: center; */
    justify-content: space-evenly;
  }
</style>
