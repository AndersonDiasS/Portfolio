<template>
  <section>
    <svg
      class="waves"
      xmlns="http://www.w3.org/2000/svg"
      xmlns:xlink="http://www.w3.org/1999/xlink"
      viewBox="0 24 150 28"
      preserveAspectRatio="none"
      shape-rendering="auto"
    >
      <defs>
        <path
          id="gentle-wave"
          d="M-160 44c30 0 58-18 88-18s 58 18 88 18 58-18 88-18 58 18 88 18 v44h-352z"
        />
      </defs>
      <g class="">
     
        <use
          xlink:href="#gentle-wave"
          x="48"
          y="7"
          class="bgPrimary"
          fill="#6011A6"
        />
      </g>
    </svg>
    <div class="bgPrimary">
      <h2 class="text-center mb-50 ">Skills</h2>

      <div class="flexCenter">
        <div class="card" v-for="card in cards" :key="card.titulo">
          <ul class="text-center">
            <li><i>{{card.titulo}}</i></li>
            <li>{{card.experiencia}}</li>
            <li>{{card.projetos}}</li>
            <li>{{card.tecnologias}}</li>
        
          </ul>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  data() {
    return {
      cards: [
        {
          titulo: 'Angular',
          experiencia: '3 anos',
          projetos: '8',
          tecnologias: 'TypeScript, SASS, HTML, Material Angular',
          icone: '',
        },
        {
          titulo: 'VueJs',
          experiencia: '1 ano',
          projetos: '1',
          tecnologias: 'Javascript, SASS, HTML, Bootstrap-Vue',
          icone: '',
        },
        {
          titulo: 'WordPress',
          experiencia: '2 anos',
          projetos: '4',
          tecnologias: 'Javascript, PHP, SCSS, HTML',
          icone: '',
        },
      ],
    }
  },
}
</script>

<style scoped>
.card ul{
  padding: 0;
}
.card ul li{
  color:#000;
  list-style-type: none;
}
</style>
