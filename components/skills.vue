<template>
  <section>
    <h2>Compétences</h2>
    <div>
      <p v-for="skill in skills" :key="skill">{{ skill }}</p>
    </div>
  </section>
</template>

<script>
export default {
  data() {
    return {
      skills: [
        "HTML5",
        "CSS3",
        "JavaScript",
        "Vue.js",
        "Nuxt.js",
        "Python",
        "PHP",
        "MySQL",
        "GitHub",
        "Git",
        "Terminal",
        "Figma",
        "Strapi",
      ],
    };
  },
};
</script>

<style scoped>
section {
  margin-top: 160px;
}

div {
  display: flex;
  gap: 40px;
  flex-wrap: wrap;
}

@media screen and (max-width: 1025px) {
  div {
    gap: 40px 30px;
  }
}

@media screen and (max-width: 850px) {
  section {
    margin-top: 120px;
  }

  div {
    gap: 30px 20px;
  }
}

@media screen and (max-width: 660px) {
  section {
    margin-top: 100px;
  }

  div {
    gap: 20px 20px;
  }
}
</style>
