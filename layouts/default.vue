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
    let img1 = new Image();
    img1.src = "/projects/latelier12/latelier12-main.webp";

    let img2 = new Image();
    img2.src = "/projects/pokemon/pokemon-main.webp";

    let img3 = new Image();
    img3.src = "/projects/journey/journey-main.webp";

    let img4 = new Image();
    img4.src = "/projects/wanned/wanned-main.webp";

    let img5 = new Image();
    img5.src = "/projects/maggle/maggle-main.webp";

    let img6 = new Image();
    img6.src = "/projects/openfoodfacts/openfoodfacts-main.webp";

    let img7 = new Image();
    img7.src = "/projects/colladraw/colladraw-main.webp";

    let img8 = new Image();
    img8.src = "/projects/mastermind/mastermind-main.webp";

    let img9 = new Image();
    img9.src = "/projects/aroundtheword/aroundtheword-main.webp";
    // img.onload = () => {
    //   console.log("img loaded");
    //   // Here you can reveal the image
    // };

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
