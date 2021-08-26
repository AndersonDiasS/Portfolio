<template>
  <!--Waves Container-->
  <section>
    <div class="TitleMenu text-center">
      <h2>Um pouco do meu trabalho</h2>
    </div>
    <div class="container flexCenter">
      <div class="card" v-for="item in items" :key="item.titulo">
        <!-- <p>{{ item.titulo }}</p> -->
        <i :class="item.icon" class="cardIcon" />
      </div>
    </div>
  </section>
  <!--Waves end-->
</template>

<script>
export default {
  data() {
    return {
      items: [
        { titulo: 'Github', descricao: '', icon: 'fab fa-github-alt' },
        { titulo: 'Code Pen', descricao: '', icon: 'fab fa-codepen' },
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

.cardIcon {
  font-size: 100px;
  padding: 25px;
}


/* Mover para o sass posteriormente  */


</style>
