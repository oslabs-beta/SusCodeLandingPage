<script lang="ts">
export default {
    name: 'Demo',
}
</script>

<template>
    <section id="demo">
      <div>
          <span class="demo-heading">DEMO</span>
      </div>
      <div>
          <img class="img" src="../../assets/images/SusCode_Demo_loop.gif" alt="SusCode Demo" />
      </div>
    </section>
</template>

<style lang="css">
#demo {
      color: #e8e8e8;
      background: linear-gradient(to bottom, #000000 0%, #242424 100%);
      display: flex;
      flex-direction: column;
      align-items: center;
      justify-content: center;
      width: 100vw;
      scroll-margin-top: 125px;
      padding-bottom: 15em;
  }

  .demo-heading {
  display: inline;
  font-size: 5rem;
  font-weight: bold;
  background: linear-gradient(142deg, rgba(122,164,212,1) 0%, rgba(4,48,111,1) 35%, rgba(4,94,222,1) 100%);
  background-clip: text;
  color: transparent;
  margin-top: -2rem;
}

.img {
    max-width: 60vw;
}
</style>