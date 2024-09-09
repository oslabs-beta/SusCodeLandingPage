<script setup lang="ts">
import NavBar from './components/Navigation/NavBar.vue'
import Main from './components/main/main.vue'
import HelloWorld from './components/HelloWorld.vue'
import About from './components/About/About.vue'
import Feature from './components/Feature/Feature.vue'
import Team from './components/Team/Team.vue'
import ContactUs from './components/Footer/ContactUs.vue'
import Footer from "./components/Footer/Footer.vue"
import Member from "./components/Team/Member.vue"
</script>

<template>
  <NavBar/>
  <div class="meat">
    <Main/>
    <HelloWorld msg="Vite + Vue" />
    <About/>
    <Feature/>
    <Team/>
    <section class="temp">
      <Member/>
      <Member msg="member2"/>
      <Member msg="member3"/>
      <Member msg="member4"/>
      <Member msg="member5"/>
    </section>
    <ContactUs/>
  </div>
  <Footer/>
</template>

<style scoped>
  .meat {
    padding: 3em;
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
