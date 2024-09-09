<script lang="ts">

export default {
    name: 'Member',
    props: {
      msg: {
        type: String,
      }
    }
}

</script>

<template>
  <section>
    <img src="../../assets/suscodeicon.png" alt="profile of someone">
    <span>{{ msg }}</span>
  </section>
</template>

<style lang="css" scoped>
  section {
    display: flex;
    flex-direction: column;
    align-items: center;
  }
  img {
    height: 12em;
    width: 12em;
    padding: 2.5em;
  }
</style>