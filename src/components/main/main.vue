<!-- main section for landing page -->

<template>
  <section id="home">
    <div className="text">
        <h1>
        A VS Code Extension
          <span class="gradient">
            Suscode
          </span>
          something
        </h1>
        <p className="mb-10 max-w-[475px] text-base leading-relaxed text-body">
        Website template and starter kit crafted to build fully functional mobile app landing pages and software websites.
        </p>

        <div className="dlButton">
          <a href="#" className="download">
            <span className="mr-[18px] border-r border-stroke border-opacity-40 pr-[18px] leading-relaxed dark:border-[#BDBDBD]">
              Download Now
            </span>
          </a>
        </div>
    </div>
    <div class="rightImg">
      <img src="" alt="catchy image for main"></img>
    </div>
  </section>
</template>

<style scoped>
  #home {
    display: flex;
    align-items: center;
    justify-content: space-around;
    flex-wrap:wrap;
    padding: 5em 10em;
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
  /* text in left */
  .gradient {
    display: inline;
    background: rgb(122,164,212);
    background: linear-gradient(142deg, rgba(122,164,212,1) 0%, rgba(4,48,111,1) 35%, rgba(4,94,222,1) 100%);
    background-clip: text;
    color: transparent;
  }

  .download {
    background-color: #f9f9f9;
    border-radius: 0.5em;
    transition: background-color 0.3s, background-color 0.3s;
    padding: 1em 1.5em;
    margin: 1em;
  }
  .download:hover {
    background-color: rgba(0, 0, 0, 0.9);
  }
</style>
