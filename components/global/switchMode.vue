<template>
  <div>
    <p v-if="active === false" @click="switchMode">{{ mode[0].light }}</p>
    <p v-if="active === true" @click="switchMode">{{ mode[1].dark }}</p>
  </div>
</template>

<script>
export default {
  data() {
    return {
      mode: [{ light: "Light" }, { dark: "Dark" }],
      active: false,
    };
  },
  methods: {
    switchMode() {
      this.active = !this.active;
      if (this.active === true) {
        document.body.classList.add("bg-light");
      } else {
        document.body.classList.remove("bg-light");
      }
    },
  },
};
</script>

<style scoped>
p {
  font-family: SCP-Regular;
  font-size: 0.813rem;
}

@media screen and (max-width: 1000px) {
  p {
    font-size: 0.713rem;
  }
}
</style>
