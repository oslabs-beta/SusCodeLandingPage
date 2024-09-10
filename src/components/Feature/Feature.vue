<script lang="ts">
export default {
    name: 'Feature',
}
</script>

<template>
    <section id="feature">
        <div className="text">
            <div class="description-container">
            <div class="descriptionBox">
                <h3>What is SusCode?</h3>
                <p>
                A VS Code Extension that scans all your previously downloaded extension
                code for potentially malicious code practices.
                </p>
            </div>

            <div class="descriptionBox">
                <h3>Why SusCode?</h3>
                <p>
                Microsoft currently does not provide very thorough security checks before
                allowing extensions to be published to the Marketplace.
                </p>
            </div>
            </div>
        </div>
    </section>
</template>

<style lang="css" scoped>
#feature {
      display: flex;
      align-items: center;
      justify-content: space-around;
      height: 100%;
  }

  .text {
    width: 100%; /* w-full */
    padding: 0 3rem;
    text-align: left;
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
</style>