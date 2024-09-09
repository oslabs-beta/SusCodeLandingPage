<script lang="ts">
import { defineComponent } from 'vue';
import Member from "./Member.vue"

export default defineComponent({
    name: 'Team',
    components: {
      Member
    }
});
</script>

<template>
  <section>
    <Member msg="Member 1"/>
    <Member msg="Member 1"/>
    <Member msg="Member 1"/>
    <Member msg="Member 1"/>
    <Member msg="Member 1"/>
  </section>
</template>

<style scoped>
  section {
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