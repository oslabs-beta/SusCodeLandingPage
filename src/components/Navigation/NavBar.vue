<script setup lang="ts">
//import { ref } from 'vue'
import ColorMode from './colormode.vue'

</script>

<template>
  <nav>
    <a href="/home" target="_blank" class="logo">
      <img src="../../assets/suscodeicon.png" class="logo" alt="SusCode logo" />
    </a>
    <a> Features </a>
    <a> About </a>
    <a> Team </a>
    <a> Contact Us </a>
    <ColorMode></ColorMode>
  </nav>
</template>

<style scoped>

nav {
  background-color: #131313;
}

.logo {
  height: 3.5em;
  will-change: filter;
  transition: filter 300ms;
}


nav {
  overflow: hidden;
  position: sticky;
  top: 0;
  width: 100vw;
  display: flex;
  align-items: center;
  justify-content: space-evenly;
  min-height: 125px;
}
nav a {
  float: left;
  color: #f2f2f2;
  text-align: center;
  padding: 14px 16px;
  text-decoration: none;
  font-size: 17px;
}
nav a:hover {
  border-radius: 1em;
  background-color: #ddd;
  color: black;
}
nav a.active {
  background-color: #646cffaa;
  color: white;
}

.logo:hover {
  filter: drop-shadow(0 0 1em #646cffaa);
  background-color: transparent;
}
</style>