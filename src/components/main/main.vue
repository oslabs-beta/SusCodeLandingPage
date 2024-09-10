<!-- main section for landing page -->

<template>
  <section id="main">
    <div className="text">
        <h1>
        A VS Code Extension
          <span class="gradient">
            Suscode
          </span>
        </h1>

        <div className="dlButton">
          <button href="#" className="download">
            Download Now
          </button>
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
  }

  .text {
    width: 100%; /* w-full */
    padding: 0 3rem;
    text-align: left;
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

  .dlButton {
    display: flex;
    align-items: center;
    justify-content: center;
  }

  .download {
    display: flex;
    align-items: center;
    justify-content: center;
    background-color: #1A1A1A;
    border-radius: 0.5em;
    transition: background-color 0.3s, background-color 0.3s;
    padding: 1em 1.5em;
    margin: 3em;
  }

  .download:hover {
    color: rgba(0, 0, 0, 0.9);
    background-color: #FFFFFFDE;
  }
</style>
