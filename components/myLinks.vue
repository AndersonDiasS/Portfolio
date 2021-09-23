<template>
  <!--Waves Container-->
  <section>
    <div class="TitleMenu text-center">
      <h2> Laboratorio 🤖</h2>
    </div>
    <div class="container flexSpaceAround">
      <a class="card" v-for="item in items" :key="item.titulo" :href="item.link" target="_blank">
        <!-- <p>{{ item.titulo }}</p> -->
        <i :class="item.icon" class="cardIcon" />
      </a>
    </div>
  </section>
  <!--Waves end-->
</template>

<script>
export default {
  data() {
    return {
      items: [
        { titulo: 'Github', descricao: '', icon: 'fab fa-github-alt', link: 'https://github.com/AndersonDiasS'},
        { titulo: 'Code Pen', descricao: '', icon: 'fab fa-codepen',  link: 'https://codepen.io/andersondiass' },
        // { titulo: 'Exemplos', descricao: '', icon: '' },
      ],
    }
  },

}
</script>
<style>

.card {
  box-shadow: 0 2px 1px -1px rgb(0 0 0 / 20%), 0 1px 1px 0 rgb(0 0 0 / 14%),
    0 1px 3px 0 rgb(0 0 0 / 12%);
  width: 250px;
}

.card:hover {
  box-shadow: 0 4px 10px 0 rgb(0 0 0 / 20%), 0 4px 20px 0 rgb(0 0 0 / 19%);
  transition: 0.5s;
}




/* Mover para o sass posteriormente  */


</style>
