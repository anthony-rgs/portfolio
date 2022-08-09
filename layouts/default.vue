<template>
  <div class="portfolio-container" :class="{ show: isActive }">
    <Navbar />
    <Nuxt />
    <Footer />
  </div>
</template>

<script>
import profile from "~/components/home/profile.vue";
export default {
  components: { profile },
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
