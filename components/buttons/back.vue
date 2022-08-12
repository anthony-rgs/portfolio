<template>
  <div>
    <a href="/" class="back-button">{{ text }}</a>
  </div>
</template>

<script>
export default {
  data() {
    return {
      text: "Retour",
    };
  },
};
</script>

<style scoped>
.back-button {
  position: fixed;
  top: 62px;
  left: 37px;

  font-family: SCP-Regular;
  font-size: 0.813rem;
}

@media screen and (min-width: 1700px) {
  .back-button {
    left: 24px;
    font-size: 20px;
    top: 90px;
  }
}

@media screen and (max-width: 1116px) {
  .back-button {
    top: 65px;
  }
}

@media screen and (max-width: 1025px) {
  .back-button {
    top: 55px;
    left: 26px;
  }
}

@media screen and (max-width: 851px) {
  .back-button {
    top: 55px;
    left: 16px;
  }
}

@media screen and (max-width: 661px) {
  .back-button {
    display: none;
  }
}
</style>
