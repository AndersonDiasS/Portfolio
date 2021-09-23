<template>
  <!--Waves Container-->
  <div class="">
    <svg
      class="waves"
      xmlns="http://www.w3.org/2000/svg"
      xmlns:xlink="http://www.w3.org/1999/xlink"
      viewBox="0 24 150 28"
      preserveAspectRatio="none"
      fill="#fff"
      shape-rendering="auto"
    >
      <defs>
        <path
          id="gentle-wave"
          d="M-160 44c30 0 58-18 88-18s 58 18 88 18 58-18 88-18 58 18 88 18 v44h-352z"
        />
      </defs>
      <g class="">
        <use xlink:href="#gentle-wave" x="48" y="7" fill="#6011A6" />
      </g>
    </svg>
    <footer class="bgPrimary">
      <br />
      <div class="flexCenter">
        <a
          v-for="footerContent in footerContents"
          :key="footerContent.content"
          :href="footerContent.link"
          target="_blank"
        >
          {{ footerContent.content }}
        </a>
      </div>
      <div class="flexCenter">
        <a
          target="_blank"
          v-for="footerLink in footerLinks"
          :key="footerLink.name"
          :href="footerLink.link"
          >{{ footerLink.name }}</a
        >
      </div>
    </footer>
  </div>
  <!--Waves end-->
</template>

<script>
export default {
  data() {
    return {
      footerContents: [
        {
          content:
            'Caso tenha interesse em saber mais sobre como foi desenvolvido esse projeto em mais detalhes pode clicar aqui. Obrigado por visitar o meu portfolio 👍',
          link: 'https://github.com/AndersonDiasS/Portfolio',
        },
      ],

      footerLinks: [
        {
          link: 'https://www.linkedin.com/in/anderson-dias-de-siqueira-770977133/',
          name: 'Linkedin',
        },
        { link: 'https://github.com/AndersonDiasS', name: 'Github' },
        { link: 'https://codepen.io/andersondiass', name: 'Codepen' },
      ],
    }
  },
}
</script>

<style>
a {
  color: white;
  transition: 0.5s;
}

a:hover {
  font-size: 1.1rem;
  color: white;
}

li {
  list-style: none;
  padding: 10px;
}
ul {
  padding-top: 40px;
}

.flexCenter a {
  margin: 10px;
}

.waves {
  position: relative;
  width: 100%;
  height: 15vh;
  /* margin-bottom:-7px; Fix for safari gap*/
  min-height: 100px;
  max-height: 150px;
}

/*Shrinking for mobile*/
@media (max-width: 768px) {
  .waves {
    height: 40px;
    min-height: 40px;
  }
  .content {
    height: 30vh;
  }
  h1 {
    font-size: 24px;
  }
}
</style>
