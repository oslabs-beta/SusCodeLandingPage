<script lang="ts">
export default {
    name: 'About',
}
</script>

<template>
    <section id="about">
        <h1>ABOUT</h1>
    </section>

    <section id="about">
        <div className="text">
            <div class="description-container">
            <div class="descriptionBox">
                <h2>What is SusCode?</h2>
                <p class="p">
                A VS Code Extension that scans all your previously downloaded extension
                code for potentially malicious code practices.
                </p>
            </div>

            <div class="descriptionBox">
                <h2>Why SusCode?</h2>
                <p class="p">
                Microsoft currently does not provide very thorough security checks before
                allowing extensions to be published to the Marketplace.
                </p>
            </div>
            </div>
        </div>
    </section>
</template>

<style lang="css">
#about {
      color: #e8e8e8;
      display: flex;
      align-items: center;
      justify-content: space-around;
      height: 100%;
      background-color: #242424;
  }

  .text {
    width: 100%; /* w-full */
    padding: 0 3rem;
    text-align: left;
    color: #e8e8e8;
  }

 .description-container {
    display: flex;
    justify-content: space-between;
    gap: 20px;
  }

  .descriptionBox {
    width: 40%;
    border-radius: 25px;
    background: #002351;
    background: linear-gradient(142deg, rgb(0, 44, 94) 0%, rgba(4,48,111,1) 35%, rgba(4,94,222,1) 100%);
    padding: 20px;
  }

  .p {
    color: #9d9d9d
  }
</style>