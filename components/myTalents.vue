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
    <div class="bgPrimary" style="padding-bottom: 20px">
      <h2 class="text-center p-t-b">Habilidades 🧙‍♂️</h2>

      <div class="flexSpaceAround container">
        <div
          class="card gradient-border"
          v-for="card in cards"
          :key="card.titulo"
        >
          <ul class="text-center">
            <li><i :class="card.icone" class="cardIcon"></i></li>
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
          titulo: 'HTML',
          experiencia: '2 anos',
          projetos: '4',
          tecnologias: 'Javascript, PHP, SCSS, HTML',
          icone: 'fab fa-html5',
        },
        {
          titulo: 'SASS',
          experiencia: '2 anos',
          projetos: '4',
          tecnologias: 'Javascript, PHP, SCSS, HTML',
          icone: 'fab fa-sass',
        },
        {
          titulo: 'Javascript',
          experiencia: '2 anos',
          projetos: '4',
          tecnologias: 'Javascript, PHP, SCSS, HTML',
          icone: 'fab fa-js-square',
        },
        {
          titulo: 'PHP',
          experiencia: '3 anos',
          projetos: '8',
          tecnologias: 'TypeScript, SASS, HTML, Material Angular',
          icone: 'fab fa-php',
        },
        {
          titulo: 'Angular',
          experiencia: '3 anos',
          projetos: '8',
          tecnologias: 'TypeScript, SASS, HTML, Material Angular',
          icone: 'fab fa-angular',
        },
        {
          titulo: 'VueJs',
          experiencia: '1 ano',
          projetos: '1',
          tecnologias: 'Javascript, SASS, HTML, Bootstrap-Vue',
          icone: 'fab fa-vuejs',
        },
        {
          titulo: 'WordPress',
          experiencia: '2 anos',
          projetos: '4',
          tecnologias: 'Javascript, PHP, SCSS, HTML',
          icone: 'fab fa-wordpress-simple',
        },
      ],
    }
  },
}
</script>

<style scoped>
.bgPrimary h2 {
  margin-bottom: 50px;
}

.card {
  margin-bottom: 30px;
  width: 230px;
}
.cardIcon {
  font-size: 60px;
}
.card ul {
  padding: 0;
  margin: 0;
}
.card ul li {
  color: #3b0a66;
  list-style-type: none;
  font-weight: bold;
  margin-top: 5px;
}

.p-t-b {
  padding-top: 20px;
  padding-bottom: 20px;
}

.gradient-border:after,
.gradient-border:hover {
  --border-width: 3px;
  transition: 1s;
  content: '';
  background: linear-gradient(
    60deg,
    hsl(224, 85%, 66%),
    hsl(269, 85%, 66%),
    hsl(314, 85%, 66%),
    hsl(359, 85%, 66%),
    hsl(44, 85%, 66%),
    hsl(89, 85%, 66%),
    hsl(134, 85%, 66%),
    hsl(179, 85%, 66%)
  );
  border-radius: var(--border-width);
  background-size: 300% 300%;
  background-position: 0 50%;
  border-radius: calc(2 * var(--border-width));
  animation: moveGradient 4s alternate infinite;
}

@keyframes moveGradient {
  50% {
    background-position: 100% 50%;
  }
}
</style>
