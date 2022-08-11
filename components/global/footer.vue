<template>
  <div>
    <p>{{ footerText }}</p>
  </div>
</template>

<script>
export default {
  data() {
    return {
      footerText: "© 2022 - Anthony Ringressi",
    };
  },
};
</script>

<style scoped>
div {
  display: flex;
  justify-content: center;
  align-items: center;
  margin-top: 160px;
}

p {
  font-size: 1rem;
}

@media screen and (max-width: 850px) {
  div {
    margin-top: 120px;
  }
}

@media screen and (max-width: 660px) {
  p {
    font-size: 1rem;
  }
}

@media screen and (max-width: 320px) {
  p {
    font-size: 0.9rem;
  }
}
</style>
