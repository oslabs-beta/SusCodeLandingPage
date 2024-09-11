<script lang="ts">
import { defineComponent } from 'vue';

export default defineComponent({
    name: 'Member',
    props: {
      name: {
        type: String,
      },
      image: {
        type: String,
        default: "suscodeicon.png"
      },
      github: {
        type: String,
      },
      linkedin: {
        type: String,
      }
    },
    methods: {
      getImgUrl(name:string):string {
        return new URL(`../../assets/${name}`, import.meta.url).href
    },
      getSocialsUrl(url:string):string {
        return new URL(`${url}`, import.meta.url).href
      }
  }
}
)
</script>

<template>
  <section>
    <!-- <img v-bind:src="image" alt="profile of someone"> -->
    <!-- <img v-bind:src="image"> -->
    <img v-bind:src="getImgUrl(image)" alt="profile of someone" /> 
    <span>{{ name }}</span>
    <div class="socials">
      <a class="githubIcon" :href=github target="_blank">
        <svg fill="#FFFFFF" xmlns="http://www.w3.org/2000/svg"  viewBox="0 0 30 30" width="30px" height="30px">    <path d="M15,3C8.373,3,3,8.373,3,15c0,5.623,3.872,10.328,9.092,11.63C12.036,26.468,12,26.28,12,26.047v-2.051 c-0.487,0-1.303,0-1.508,0c-0.821,0-1.551-0.353-1.905-1.009c-0.393-0.729-0.461-1.844-1.435-2.526 c-0.289-0.227-0.069-0.486,0.264-0.451c0.615,0.174,1.125,0.596,1.605,1.222c0.478,0.627,0.703,0.769,1.596,0.769 c0.433,0,1.081-0.025,1.691-0.121c0.328-0.833,0.895-1.6,1.588-1.962c-3.996-0.411-5.903-2.399-5.903-5.098 c0-1.162,0.495-2.286,1.336-3.233C9.053,10.647,8.706,8.73,9.435,8c1.798,0,2.885,1.166,3.146,1.481C13.477,9.174,14.461,9,15.495,9 c1.036,0,2.024,0.174,2.922,0.483C18.675,9.17,19.763,8,21.565,8c0.732,0.731,0.381,2.656,0.102,3.594 c0.836,0.945,1.328,2.066,1.328,3.226c0,2.697-1.904,4.684-5.894,5.097C18.199,20.49,19,22.1,19,23.313v2.734 c0,0.104-0.023,0.179-0.035,0.268C23.641,24.676,27,20.236,27,15C27,8.373,21.627,3,15,3z"/></svg>
      </a>
      
      <a class="linkedin" :href=linkedin target="_blank">
        <svg version="1.1" id="Capa_1" xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" viewBox="0 0 455.731 455.731" xml:space="preserve" width="25px" height="25px" fill="#000000"><g id="SVGRepo_bgCarrier" stroke-width="0"></g><g id="SVGRepo_tracerCarrier" stroke-linecap="round" stroke-linejoin="round"></g><g id="SVGRepo_iconCarrier"> <g> <rect x="0" y="0" style="fill:#0084B1;" width="455.731" height="455.731"></rect> <g> <path style="fill:#FFFFFF;" d="M107.255,69.215c20.873,0.017,38.088,17.257,38.043,38.234c-0.05,21.965-18.278,38.52-38.3,38.043 c-20.308,0.411-38.155-16.551-38.151-38.188C68.847,86.319,86.129,69.199,107.255,69.215z"></path> <path style="fill:#FFFFFF;" d="M129.431,386.471H84.71c-5.804,0-10.509-4.705-10.509-10.509V185.18 c0-5.804,4.705-10.509,10.509-10.509h44.721c5.804,0,10.509,4.705,10.509,10.509v190.783 C139.939,381.766,135.235,386.471,129.431,386.471z"></path> <path style="fill:#FFFFFF;" d="M386.884,241.682c0-39.996-32.423-72.42-72.42-72.42h-11.47c-21.882,0-41.214,10.918-52.842,27.606 c-1.268,1.819-2.442,3.708-3.52,5.658c-0.373-0.056-0.594-0.085-0.599-0.075v-23.418c0-2.409-1.953-4.363-4.363-4.363h-55.795 c-2.409,0-4.363,1.953-4.363,4.363V382.11c0,2.409,1.952,4.362,4.361,4.363l57.011,0.014c2.41,0.001,4.364-1.953,4.364-4.363 V264.801c0-20.28,16.175-37.119,36.454-37.348c10.352-0.117,19.737,4.031,26.501,10.799c6.675,6.671,10.802,15.895,10.802,26.079 v117.808c0,2.409,1.953,4.362,4.361,4.363l57.152,0.014c2.41,0.001,4.364-1.953,4.364-4.363V241.682z"></path> </g> </g> </g></svg>
      </a>
    </div>
  </section>
</template>

<style lang="css" scoped>
  section {
    display: flex;
    flex-direction: column;
    align-items: center;
    color: rgba(255, 255, 255, 0.65);
    font-size: 1.5rem;
    margin: 2rem;
  }
  span {
    padding: 1em;
  }
  img {
    height: 15rem;
    width: 15rem;
    border-radius: 50%;
    transition: all ease 0.5s;
  }

  html.cafe img {
  filter: sepia(0) hue-rotate(55deg) brightness(1) !important;
}

html.contrast img {
  filter: contrast(.5);
}

/* .linkedin:hover {
  filter: drop-shadow(0 0 1em #646cffaa);
  background-color: transparent;
} */

svg {
  transition: all ease 0.5s;
}

svg:hover, img:hover {
  transform: translateY(-3px);
  box-shadow: 0px 15px 25px #535bf2;
  }

.socials {
  /* WHY MARGIN NO WORK not important */
  display: grid;
  grid-template-columns: auto auto;
  width: 80px;
}
</style>