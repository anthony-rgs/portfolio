<template>
  <section>
    <h2>{{ title }}</h2>
    <p>{{ text }}</p>
  </section>
</template>

<script>
export default {
  props: {
    title: String,
    text: String,
  },
};
</script>

<style scoped>
@media screen and (max-width: 900px) {
  section {
    margin-top: 120px;
  }
}

@media screen and (max-width: 661px) {
  section {
    margin-top: 100px;
  }
}
</style>
