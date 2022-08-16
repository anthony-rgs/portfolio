<script>
export default {
  mounted() {
    let img = new Image();
    img.onload = () => {
      console.log("img loaded");
      // Here you can reveal the image
    };
    img.src = "/projects/mastermind/mastermind-main.webp";
  },
};
</script>
