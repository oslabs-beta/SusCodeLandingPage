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
      <div class="content">
        <h1>A VS Code Extension</h1>
        <span class="gradient">Suscode</span>
        <p class="body">
          A VS Code Extension designed to scan your downloaded extensions for potentially harmful code practices.
        </p>
        <div class="buttons">
          <button href="#" class="download">Download Now</button>
          <button class="features">How SusCode Works</button>
        </div>
      </div>
    </div>
    <img src="../../assets/skyline-rat-signal.png" class="logo" alt="SusCode logo" />
  </section>
</template>

<style scoped>

/* Spotlight effect styles */
.dim-overlay {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background-color: rgba(0, 0, 0, 0.8);
  z-index: 1001; /* On top of everything */
}

.spotlight {
  position: absolute;
  width: 200px;
  height: 200px;
  background: radial-gradient(circle, rgba(255, 255, 255, 0.3) 20%, rgba(0, 0, 0, 0) 80%);
  border-radius: 50%;
  pointer-events: none;
  transition: top 0.5s ease, left 0.5s ease;
  z-index: 1002;
}

/* Main section */
#main {
  display: flex;
  align-items: center;
  justify-content: center;
  height: 85vh;
  overflow: hidden; /* Prevent scrolling */
  margin-left:3em;
}

.text {
  display: flex;
  /* grid-template-columns: 1fr 1fr; */
  align-items: center;
  justify-items: center;
  width: 100%;
  height: 100%;
  padding: 0 1em 2em 3em;
  margin: 0;
  box-sizing: border-box;
}

img {
  width: 65%;
}

@media(max-width: 950px) {
  #main {
    margin: 0;
    flex-wrap: wrap;
  };
  .text {
    padding: 0;
  }
  /* img {
    width: 100%;
  } */
}

.content {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  text-align: center;
  color: #e8e8e8;
  padding: 1rem;
}

/* .logo {
  display: block;
  max-width: 60%;
  max-height: 60%;
  object-fit: contain;
} */

h1 {
  z-index: 5;
  margin: 0;
  padding: 0;
  color: #9d9d9d;
}

.gradient {
  display: inline;
  font-size: 5rem;
  font-weight: bold;
  background: linear-gradient(142deg, rgba(122,164,212,1) 0%, #747bff 25%, #f2c300 50%, rgba(4,48,111,1) 75%, #003366 100%);
  background-size: 350% 350%;
  animation: gradient 20s ease infinite;
  background-clip: text;
  color: transparent;
  margin-top: -2rem;
}

@keyframes gradient {
	0% {
		background-position: 0% 50%;
	}
	50% {
		background-position: 100% 50%;
	}
	100% {
		background-position: 0% 50%;
	}
}

.buttons {
  display: flex;
  gap: 1rem;
  justify-content: center;
  margin-top: 1rem;
}

/* Button styles */
.download, .features {
  padding: 0.75em 1.5em;
  border-radius: 0.5rem;
  transition: background-color 0.3s ease;
}

.download {
  background-color: rgba(4, 94, 222, 1);
}

.download:hover {
  background-color: #1A1A1A;
}

/* do we need this button? */
.features {
  background-color: #1A1A1A;
}
.features:hover {
  background-color: rgba(4, 94, 222, 1);
}

.body {
  color: #9d9d9d;
  font-size: 1rem;
}

/* @media (min-width: 768px) {
  #main {
    display:flex;
    flex-wrap: wrap;
    flex-grow: 1;
  }
} */

/* MAKE IMAGE WRAP WHY NO WRAP */
@media (max-width: 768px) {
  #main {
    display:flex;
    flex-wrap: wrap;
    flex-grow: 1;
  }
  
}
</style>