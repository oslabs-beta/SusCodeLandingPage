<script setup lang="ts">
</script>

<template>
  <nav>
    <a href="/home" class="logo">
      <img src="../../assets/images/suscodeicon.png" class="logo" alt="SusCode logo" />
    </a>
    <a href="#about"> About </a>
    <a href="#features"> Features </a>
    <a href="#demo">Demo</a>
    <a href="#team"> Team </a>
    <a href="#contactus"> Contact Us </a>
  </nav>
</template>

<style scoped>
.logo {
  height: 3.5em;
  will-change: filter;
  transition: filter 300ms;
  align-items: center;
  justify-content: center;
}

nav {
  background-color: #242424;
  color: rgb(93, 93, 93); 
  overflow: hidden;
  position: sticky;
  top: 0;
  width: 100vw;
  display: flex;
  align-items: center;
  justify-content: space-evenly;
  min-height: 125px;
  z-index: 1000;
}
nav a {
  float: left;
  color: #f2f2f2;
  text-align: center;
  padding: 0px 16px;
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