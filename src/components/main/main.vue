<script lang="ts">
import { ref, onMounted } from 'vue';

export default {
  name: 'Main',
  setup() {
    const showSpotlight = ref(true);
    const spotlightStyle = ref({});

    onMounted(() => {
      let spotlightX = 0;
      let spotlightY = 0;
      const spotlightDuration = 4000;

      const interval = setInterval(() => {
      // Randomly move the spotlight around the screen
      spotlightX = Math.random() * window.innerWidth;
      spotlightY = Math.random() * window.innerHeight;

      spotlightStyle.value = {
        top: `${spotlightY}px`,
        left: `${spotlightX}px`,
      };
    }, 300);

      // Stop the spotlight after a few seconds
      setTimeout(() => {
        clearInterval(interval);
        showSpotlight.value = false;
      }, spotlightDuration);
    });

    return {
      showSpotlight,
      spotlightStyle,
    };
  },
};
</script>

<template>
  <div class="dim-overlay" v-if="showSpotlight">
      <div class="spotlight" :style="spotlightStyle"></div>
  </div>

  <section id="main">
    <div class="text">
      <h1>
        A VS Code Extension
        <span class="gradient">Suscode</span>
      </h1>
      <p class="body">
        A VS Code Extension designed to scan your downloaded extensions for potentially harmful code practices.
      </p>

      <div class="button">
        <button href="#" class="download">Download Now</button>
        <button class="features">How SusCode Works</button>
      </div>
    </div>
  </section>
</template>

<style scoped>
#main {
  display: flex;
  align-items: center;
  justify-content: space-around;
  height: 100%;
  position: relative;
}

.dim-overlay {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background-color: rgba(0, 0, 0, 0.8);
  z-index: 10; /* On top of everything */
}

.spotlight {
  position: absolute;
  width: 200px;
  height: 200px;
  background: radial-gradient(circle, rgba(255, 255, 255, 0.3) 20%, rgba(0, 0, 0, 0) 80%);
  border-radius: 50%;
  pointer-events: none;
  transition: top 0.5s ease, left 0.5s ease;
  z-index: 11;
}

.text {
  width: 100%;
  padding: 0 3rem;
  text-align: left;
  z-index: 1; /* Make sure text is behind the spotlight */
}

  @media (min-width: 1024px) { /* breakpoint: 1024px and up */
    .text {
      width: 58.333333%; /* w-7/12 */
    }
  }

  .gradient {
    display: inline;
    background: rgb(122,164,212);
    background: linear-gradient(142deg, rgba(122,164,212,1) 0%, rgba(4,48,111,1) 35%, rgba(4,94,222,1) 100%);
    background-clip: text;
    color: transparent;
  }

  .button {
    display: flex;
    align-items: center;
    justify-content: center;
  }

  .download {
    display: flex;
    align-items: center;
    justify-content: center;
    background-color: rgba(4,94,222,1);
    border-radius: 0.5em;
    transition: background-color 0.3s, background-color 0.3s;
    padding: 1em 1.5em;
    margin: 3em;
  }

  .download:hover {
    background-color: #1A1A1A;
  }

  .features {
    display: flex;
    align-items: center;
    justify-content: center;
    background-color: #1A1A1A;
    border-radius: 0.5em;
    transition: background-color 0.3s, background-color 0.3s;
    padding: 1em 1.5em;
    margin: 3em;
  }

  .features:hover {
    background-color: rgba(4,94,222,1);
  }

  .body {
    color: #9d9d9d;
  }
</style>