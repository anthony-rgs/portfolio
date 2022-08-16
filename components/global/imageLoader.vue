<template></template>

<script>
export default {
  props: {
    image: String,
  },
  mounted() {
    for (let i = 0; i < 1; i++) {
      const image = new Image();
      image.src = this.image;
    }
  },
};
</script>
