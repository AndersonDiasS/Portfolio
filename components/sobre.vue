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
      <article class="mb-50" style="width: 100%">
        Lorem ipsum dolor sit amet, consectetur adipiscing elit. Suspendisse
        tempor elementum est, in laoreet metus egestas suscipit. Curabitur
        porttitor pellentesque enim, vel lacinia mi varius luctus. Mauris lorem
        arcu, ullamcorper quis mauris vel, tincidunt viverra arcu. Pellentesque
        vel molestie eros. Donec ullamcorper odio eget neque eleifend facilisis.
        Quisque eros elit, mattis in elit a, gravida auctor urna. Sed
        sollicitudin lectus a sapien convallis, sit amet vestibulum ipsum
        ullamcorper. Duis lobortis condimentum libero vitae pulvinar. Donec at
        elementum leo. Quisque condimentum faucibus magna, eu tincidunt odio
        tincidunt eu. Integer rhoncus, leo a viverra dapibus, augue felis
        bibendum turpis, vitae aliquet purus purus malesuada ligula. Nunc
        elementum molestie ante a finibus. Fusce neque erat, ornare quis felis
        vitae, interdum sodales nunc.
      </article>

      <div
        id=""
        class="littleImage"
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
        { nome: 'Employer RH', img: require('@/assets/IMG/Employer.jpg') },
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
.littleImage {
  width: 100px;
  align-items: center;
  display: flex;
}

.companies img {
  width: 100%;
}
</style>
