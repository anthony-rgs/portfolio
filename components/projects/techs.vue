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
