<template>
  <section class="section gallery">
    <h2>{{ title }}</h2>
    <div class="container">
      <img
        v-for="(image, indice) in images"
        :key="indice"
        :src="image.url"
        alt="Project image"
      />
    </div>
  </section>
</template>

<script>
export default {
  props: {
    images: Array,
  },
  data() {
    return {
      title: "Galerie",
    };
  },
};
</script>

<style scoped>
.container {
  display: flex;
  justify-content: space-between;
  flex-wrap: wrap;
}

.gallery {
  margin-bottom: -50px;
}

.container img {
  width: 48%;
  margin-bottom: 50px;
}

img:nth-child(2) {
  padding-bottom: 0px;
}

@media screen and (max-width: 661px) {
  .container img {
    width: 100%;
    margin-bottom: 20px;
  }

  .container img:last-child {
    margin-bottom: 0px;
  }
}
</style>
