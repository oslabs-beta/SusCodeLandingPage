<script lang="ts">
export default {
    name: 'About',
}
</script>

<template>
    <section id="about">
        <div>
            <span class="about-heading">ABOUT</span>
        </div>
    
        <div className="text">
            <div class="description-container">
                <span class="about-span">
                    SusCode is a VScode extension built to help every VScode user take the security of their extensions into their own hands. SusCode counteracts both the lack of an extensive permissions protocol and the low threshold for extension security in Microsoft’s Visual Studio Marketplace by searching through your already downloaded extensions and making you aware of patterns, packages, and requests that could increase an extension’s vulnerability to malicious attacks. SusCode stands out as the first application meeting this need within the VScode community.
                </span>
            </div>
        </div>

        <div>
            <h1>HOW IT WORKS</h1>
            <hr>
            <p>When you download an extension for VScode, that extension’s source code is stored on your local device. SusCode then does the follow to easily bring potential vulnterabilities to your attention:</p>
        </div>

        <div class="works">
            <div>
                <span class="works-span">SusCode provides a list of your installed extensions, you choose which extension(s) you want to scan.</span>
                <span class="works-span">For each extension you select, Suscode provides a brief description of the extension (grabbed from it’s own ReadMe.md!) and displays the frequency of each pattern found.</span>
                <span class="works-span">SusCode then completes a series of scans and produces a detailed report of the results of the scan for each extension.</span>
            </div>
        </div>
    </section>
</template>

<style lang="css">
#about {
      color: #e8e8e8;
      background: linear-gradient(to bottom, #000000 0%, #242424 100%);
      display: flex;
      flex-direction: column;
      align-items: center;
      justify-content: center;
      width: 100vw;
      scroll-margin-top: 125px;
      /* background-color: #242424; */
  }

  .about-heading {
  display: inline;
  font-size: 5rem;
  font-weight: bold;
  background: linear-gradient(142deg, rgba(122,164,212,1) 0%, rgba(4,48,111,1) 35%, rgba(4,94,222,1) 100%);
  background-clip: text;
  color: transparent;
  margin-top: -2rem;
}

  .text {
    width: 100%; /* w-full */
    padding: 0 3rem;
    text-align: left;
    color: #e8e8e8;
  }

 .description-container {
    display: flex;
    align-items: center;
    justify-content: center;
    gap: 20px;
    margin-bottom: 4rem;
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

  .about-span {
    height: 200px;
    width: 60vw;
    background: linear-gradient(142deg, rgb(0, 44, 94) 0%, rgba(4,48,111,1) 35%, rgba(4,94,222,1) 100%);
    border-radius: 10px;
    display: flex;
    justify-content: center;
    align-items: center;
    flex-direction: column;
    padding: 2em;
    box-shadow: 0px 5px 20px rgb(0, 44, 94), 0px 5px 20px #fff;
    transition: all ease 0.5s;
    color: #fff;
  }

  .about-span:hover {
  transform: translateY(-10px);
  box-shadow: 0px 15px 30px #fff;
  }

  .about-span span {
    font-size: 1rem;
    font-weight: 600;
    text-align: center;
  }

  .works {
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
  align-items: center;
  width: 100vw;
  padding: 2rem;
  box-sizing: border-box;
}

.works div {
  display: flex;
  justify-content: center;
  flex-wrap: wrap;
  width: 100%;
  gap: 1.5rem;
}

.works-span {
  background: linear-gradient(142deg, rgb(0, 44, 94) 0%, rgba(4,48,111,1) 35%, rgba(4,94,222,1) 100%);
  border-radius: 10px;
  width: 25%;
  min-width: 250px;
  padding: 2em;
  box-shadow: 0px 5px 20px rgb(0, 44, 94), 0px 5px 20px #fff;
  transition: all ease 0.5s;
  color: #fff;
  margin: 1rem;
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
}

.works-span:hover {
  transform: translateY(-10px);
  box-shadow: 0px 15px 30px #fff;
}

.works-span span {
  font-size: 1rem;
  font-weight: 600;
}
</style>