<script setup lang="ts"></script>

<template>
  <nav>
    <a href="/home" class="logo">
      <img
        src="../../assets/images/suscodeicon.png"
        class="logo"
        alt="SusCode logo"
      />
    </a>
    <a class="navButs" href="#about"> About </a>
    <a class="navButs" href="#features"> Features </a>
    <a class="navButs" href="#demo">Demo</a>
    <a class="navButs" href="#team"> Team </a>
    <a class="navButs" href="#contactus"> Contact Us </a>
  </nav>
</template>

<style scoped>
.logo {
  padding-top: 0px;
  height: 3.5em;
  will-change: filter;
  transition: filter 300ms;
  align-items: center;
  justify-content: center;
}

.navButs:hover {
  color: #FFDE59;
  /* box-shadow: 0 0 20px #FFDE59; */
  text-shadow: 0 0 5px #FFDE59;
}
nav {
  background-color: rgba(36, 36, 36, 0.7);
  /* background-color: rgba(36, 36, 36, 1); */
  color: rgb(93, 93, 93);
  overflow: hidden;
  position: sticky;
  top: 0;
  width: 100vw;
  display: flex;
  align-items: center;
  padding: 0 20px;
  justify-content: space-evenly;
  min-height: 125px;
  z-index: 1000;
  background: linear-gradient(to bottom, rgba(36, 36, 36, 0.9) 95%, rgba(36, 36, 36, 0));
}
nav a {
  /* float: left; */
  color: #f2f2f2;
  text-align: center;
  padding: 12px 20px;
  text-decoration: none;
  font-size: 20px;
  
  border-radius: 8px;
  transition: background-color 0.3s ease, color 0.3s ease;
  /* border: red; */
  /* border-width: 1px;
  border-style: solid; */
}
nav a:hover {
  border-radius: 1em;
  /* background-color: #ddd;
  color: black; */
  
}
nav a.active {
  background-color: #646cffaa;
  color: white;
}

.logo:hover {
  filter: drop-shadow(0 0 7px #FFDE59);
  background-color: transparent;
}
</style>
