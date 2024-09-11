<script lang="ts">
export default {
    name: 'ContactUs',
}
</script>

<template>
    <section id="contactus">
      <div class="contact-container">
        <span class="contact-span">
          Contact Us: <a href= "mailto: suscodeapp@gmail.com"> suscodeapp@gmail.com </a>
        </span>
      </div>
    </section>
</template>

<style lang="css">
  #contactus {
    font-size: 2.5em;
    color:antiquewhite;
    padding: 3em;
  }

  .contact-container {
    display: flex;
    align-items: center;
    justify-content: center;
    gap: 20px;
    margin-bottom: 4rem;
  }

  .contact-span {
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

  .contact-span:hover {
  transform: translateY(-10px);
  box-shadow: 0px 15px 30px #fff;
  }

  .contact-span span {
    font-size: 1rem;
    font-weight: 600;
    text-align: center;
  }
</style>