<template>
  <section>
    <h2>Rôle</h2>
    <p>{{ text }}</p>
  </section>
</template>

<script>
export default {
  props: {
    text: String,
  },
};
</script>
