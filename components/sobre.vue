<template>
  <section class="">
    <svg
      class="waves bgPrimary"
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
        <use xlink:href="#gentle-wave" x="48" y="7" class="" fill="#fff" />
      </g>
    </svg>

    <h2 class="TitleMenu text-center">Um pouco mais sobre mim 🐧</h2>
    <div class="flexSpaceEvenly container">
      <article class="mb-50">
        Formado em Sistemas para Web na Faculdade Padre João Bagozzi, comecei a
        minha caminhada no mercado trabalhando como Estagiário a Web Design na Employer, lá
        eu auxiliava na construção de Layouts, Produção gráfica e fazia as
        manutenções nos próprios sistemas internos da empresa. Após isso fui
        convidado a trabalhar com a FASO - Fabrica de software, onde atuei como
        Front end e Web Designer desenvolvendo Layouts para diversos aplicativos
        e Web sites, além de trabalhar como social Media. Saindo de lá acabei
        trabalhando como Desenvolvedor Front end na Hero Spark no setor de
        Marketing, elaborando landing pages e desenvolvendo e customizando
        paginas Wordpress em conjunto com a minha equipe.
      </article>

      <div
        id=""
        class="littleImage mb-50"
        v-for="empresa in empresas"
        :key="empresa.nome"
      >
        <img class="littleImage" :src="empresa.img" v-bind:alt="empresa.nome" />
      </div>
    </div>
  </section>
</template>
<script>
export default {
  data() {
    return {
      empresas: [
        { nome: 'Employer RH', img: require('@/assets/IMG/employer.png') },
        {
          nome: 'FASO Fabrica de software',
          img: require('@/assets/IMG/FASO.jpg'),
        },
        { nome: 'Hero Spark', img: require('@/assets/IMG/Herospark.png') },
      ],
    }
  },
}
</script>

<style scoped>
article {
  width: 100%;
  border-bottom: 1px solid #ddd;
  padding-bottom: 30px;
}

.littleImage {
  width: 100px;
  align-items: center;
  display: flex;
  height: 100%;
  align-items:center;
}

.companies img {
  width: 100%;
}
</style>
