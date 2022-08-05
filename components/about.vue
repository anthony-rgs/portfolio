<template>
  <section class="about">
    <h2>À propos</h2>
    <p>
      Salut, j'ai 23 ans et j'habite à Paris. Je suis actuellement étudiant en
      première année à HETIC, dans un bachelor développement web.
    </p>
    <p>
      Je suis arrivé en ocobre 2021 dans la programmation après une
      réorientation d'une licence d'Espagnol et études internationales à la
      Sorbonne. J'ai fait ce choix parce que la programmation m'a toujours
      interessé et c'est un milieu qui me pousse à me surpasser et à donner le
      meilleur de moi même sur chaque projet que j'entreprend.
    </p>
    <a class="link" href="/cv-ringressi-anthony.pdf" download
      >Télécharger mon cv.</a
    >
  </section>
</template>

<script>
export default {};
</script>

<style scoped>
.about {
  width: 790px;
  margin-top: 120px;
}

p:nth-child(3) {
  margin: 40px 0;
}

@media screen and (max-width: 1025px) {
  .about {
    width: 650px;
  }
}

@media screen and (max-width: 850px) {
  .about {
    width: 100%;
    margin-top: 100px;
  }

  p:nth-child(3) {
    margin: 30px 0;
  }
}

@media screen and (max-width: 660px) {
  .about {
    margin-top: 100px;
  }

  p:nth-child(3) {
    margin: 20px 0;
  }
}
</style>
