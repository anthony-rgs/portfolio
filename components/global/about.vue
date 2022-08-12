<template>
  <section class="about">
    <h2>{{ title }}</h2>
    <p v-html="text"></p>
  </section>
</template>

<script>
export default {
  data() {
    return {
      title: "À propos",
    };
  },
  props: {
    text: String,
  },
};
</script>

<style scoped>
.about {
  width: 790px;
  margin-top: 120px;
}

p {
  margin-bottom: 40px;
}

@media screen and (min-width: 1700px) {
  .about {
    width: 70%;
    margin-top: 200px;
  }

  p {
    margin-bottom: 100px;
  }
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

  p {
    margin-bottom: 30px;
  }
}

@media screen and (max-width: 660px) {
  .about {
    margin-top: 100px;
  }

  p {
    margin-bottom: 20px;
  }
}
</style>
