<template>
  <section class="section">
    <h2>{{ title }}</h2>
    <div>
      <p v-for="skill in skills" :key="skill">{{ skill }}</p>
    </div>
  </section>
</template>

<script>
export default {
  data() {
    return {
      title: "Compétences",
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
  div {
    gap: 30px 20px;
  }
}

@media screen and (max-width: 660px) {
  div {
    gap: 20px 20px;
  }
}
</style>
