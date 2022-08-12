<template>
  <client-only>
    <tbody class="portfolio-container" :class="{ show: isActive }">
      <SwitchMode />
      <Nuxt />
      <Footer />
    </tbody>
  </client-only>
</template>

<script>
export default {
  data() {
    return {
      isActive: false,
    };
  },
  methods: {
    checkStatus() {
      if (process.client) {
        if (localStorage.getItem("lightMode") === "true") {
          document.body.classList.add("bg-light");
        }
      }
    },
  },
  mounted() {
    if (localStorage.getItem("lightMode") === null) {
      localStorage.setItem("lightMode", "false");
    }
    this.isActive = true;
    this.checkStatus();
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
