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
  <!-- Spotlight Overlay -->
  <div class="dim-overlay" v-if="showSpotlight">
    <div class="spotlight" :style="spotlightStyle"></div>
  </div>

  <!-- Main Section -->
  <section id="main">
    <div class="text">
      <img src="../../assets/skyline-rat-signal.png" class="logo" alt="SusCode logo" />
        <h1>A VS Code Extension</h1>
        <span class="gradient">Suscode</span>
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
html, body {
  height: 100%;
  margin: 0;
  padding: 0;
  overflow-x: hidden;
}

/* Spotlight effect styles */
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

/* Main section */
#main {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  height: 100vh;
  width: 100vw;
  padding: 0;
  margin: 0;
  position: relative;
  background-color: #242424;
  overflow: hidden; /* Prevent scrolling */
}

.text {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  text-align: center;
  background: linear-gradient(to bottom, #131313 0%, #242424 100%);
  color: #e8e8e8;
  width: 100%;
  height: 100%;
  padding: 0;
  margin: 0;
  box-sizing: border-box;
  overflow: hidden;
}

.logo {
  display: block;
  max-width: 60%;
  max-height: 60%;
  object-fit: contain;
  margin-bottom: -2rem; /* Adjust overlap with h1 */
}

h1 {
  z-index: 1;
  margin: 0;
  padding: 0;
  color: #9d9d9d;
}

.gradient {
  display: inline;
  font-size: 5rem;
  font-weight: bold;
  background: linear-gradient(142deg, rgba(122,164,212,1) 0%, rgba(4,48,111,1) 35%, rgba(4,94,222,1) 100%);
  background-clip: text;
  color: transparent;
  margin-top: -2rem;
}

.button {
  display: flex;
  gap: 1rem;
  justify-content: center;
  margin-top: 1rem;
}

/* Button styles */
.download, .features {
  padding: 0.75em 1.5em;
  font-size: 1rem;
  border-radius: 0.5rem;
  transition: background-color 0.3s ease;
}

.download {
  background-color: rgba(4, 94, 222, 1);
}

.download:hover {
  background-color: #1A1A1A;
}

.features {
  background-color: #1A1A1A;
}

.features:hover {
  background-color: rgba(4, 94, 222, 1);
}

.body {
  color: #9d9d9d;
  font-size: 1rem;
  width: 50vh;
}

@media (min-width: 768px) {
  h1 {
    font-size: 3.25rem;
  }

  .gradient {
    font-size: 5rem;
  }

  .download, .features {
    font-size: 1.25rem;
    padding: 1em 2em;
  }

  .logo {
    max-width: 60vw;
    max-height: 60vh;
  }
}
</style>