<script lang="ts">
  import Member from "./Member.vue"
</script>

<template>
  <section>
    <Member></Member>
    <Member></Member>
    <Member></Member>
    <Member></Member>
    <Member></Member>
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