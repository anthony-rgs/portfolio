<template></template>

<script>
export default {
  props: {
    images: Array,
  },
  mounted() {
    for (let i = 0; i < this.images.length; i++) {
      const image = new Image();
      image.src = this.images[i];
    }
  },
};
</script>
