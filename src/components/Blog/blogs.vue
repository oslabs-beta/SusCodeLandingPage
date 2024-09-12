<script lang="ts">
export default {
    name: 'blogs',
}
</script>

<template>
    <section id="blog">
        <div>
            <span class="blog-heading">BLOGS</span>
        </div>

      <div class="blogdes">
        <p>Check out our various publications and blog posts!</p>
        <hr>
      </div>

        <div class="blogs">
            <div>
                <a class="blogs-span" href="https://medium.com/@allisonrm95/suscode-a-timely-solution-to-rising-vs-code-extension-security-concerns-44cbe06378fd"><span>Check out our Medium Article!</span></a>
                <a class="blogs-span" href=""><span>See a Reddit thread about us!</span></a>
            </div>
        </div>

        <div class="blogs">
            <div>
                <a class="blogs-span" href=""><span>Published on Hacker News!</span></a>
                <a class="blogs-span" href="https://www.producthunt.com/posts/suscode?embed=true&utm_source=badge-featured&utm_medium=badge&utm_souce=badge-suscode"><span>Published on Product Hunt!</span></a>
            </div>
        </div>

    </section>
</template>

<style lang="css" scoped>
#blog {
    background: linear-gradient(to bottom, #000000 25%, #242424 100%);
      display: flex;
      flex-direction: column;
      align-items: center;
      justify-content: center;
      width: 100vw;
      height: 100vh;
  }

  .blog-heading {
  display: inline;
  font-size: 5rem;
  font-weight: bold;
  background: linear-gradient(142deg, rgba(122,164,212,1) 0%, rgba(4,48,111,1) 35%, rgba(4,94,222,1) 100%);
  background-clip: text;
  color: transparent;
  margin-top: -2rem;
}

  .blog-span {
    height: 80vh;
    width: 60vw;
    background: linear-gradient(142deg, rgb(0, 44, 94) 0%, rgba(4,48,111,1) 35%, rgba(4,94,222,1) 100%);
    border-radius: 10px;
    display: flex;
    justify-content: center;
    font-size: large;
    align-items: center;
    flex-direction: column;
    padding: 2em;
    box-shadow: 0px 5px 20px rgb(0, 44, 94), 0px 5px 20px #fff;
    transition: all ease 0.5s;
    color: #fff;
  }

  .blog-span:hover {
  transform: translateY(-10px);
  box-shadow: 0px 15px 30px #fff;
  }

  .blog-span span {
    font-size: 1rem;
    font-weight: 600;
    text-align: center;
  }

  .blogs {
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
  align-items: center;
  width: 100vw;
  padding: 2rem;
  box-sizing: border-box;
}

.blogs div {
  display: flex;
  justify-content: center;
  flex-wrap: wrap;
  width: 100%;
  gap: 1.5rem;
}

.blogs-span {
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

.blogs-span:hover {
  transform: translateY(-10px);
  box-shadow: 0px 15px 30px #fff;
}

.blogs-span span {
  font-size: 1.25rem;
  font-weight: 600;
}

.text {
  color: rgb(189, 189, 189);
  display: flex;
  align-items: center;
  justify-content: center;
}

hr {
  color: white;
}

.blogdes {
  width:60%;
}


</style>