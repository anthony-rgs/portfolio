<template>
  <div>
    <p>© 2022 - Anthony Ringressi</p>
  </div>
</template>

<script>
export default {};
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
    font-size: 0.9rem;
  }
}
</style>
