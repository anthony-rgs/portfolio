<template>
  <section>
    <h2>Projets</h2>
    <div class="project-container">
      <img src="~assets/images/latelier12-main.webp" alt="L'Atelier Image" />
      <div class="bar"></div>
      <div class="text-container">
        <p>
          Premier projet professionnel qui consistait à la conception et
          réalisation d’un site vitrine pour un salon de coiffure.
        </p>
        <a class="link" href="">Voir le projet.</a>
      </div>
    </div>
  </section>
</template>

<script>
export default {};
</script>

<style scoped>
section {
  margin-top: 160px;
}

.project-container {
  display: flex;
  justify-content: space-between;
}

img {
  width: 575px;
  height: 100%;
}

.bar {
  height: 328px;
  width: 3px;
}

.text-container {
  width: 500px;
  display: flex;
  flex-direction: column;
  justify-content: space-between;
}

a {
  width: fit-content;
}
</style>
