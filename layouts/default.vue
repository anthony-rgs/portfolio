<template>
  <div class="portfolio-container" :class="{ show: isActive }">
    <SwitchMode />
    <Nuxt />
    <Footer />
  </div>
</template>

<script>
export default {
  data() {
    return {
      isActive: false,
    };
  },
  mounted() {
    this.isActive = true;
  },
};
</script>

<style>
.portfolio-container {
  opacity: 0;
}

.show {
  opacity: 1;
  transition: opacity 0.7s ease;
}
</style>
