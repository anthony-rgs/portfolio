<template>
  <div>
    <p class="light" v-if="active === false" @click="switchMode">
      {{ mode[0].light }}
    </p>
    <p class="dark" v-if="active === true" @click="switchMode">
      {{ mode[1].dark }}
    </p>
  </div>
</template>

<script>
export default {
  data() {
    return {
      mode: [{ light: "Clair" }, { dark: "Sombre" }],
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
.light,
.dark {
  position: fixed;
  top: 50px;
}

.light {
  right: 40px;
}

.dark {
  right: 37px;
}

p {
  font-family: SCP-Regular;
  font-size: 0.813rem;
}

@media screen and (max-width: 1025px) {
  .light {
    right: 30px;
  }

  .dark {
    right: 27px;
  }
}

@media screen and (max-width: 851px) {
  .light {
    right: 20px;
  }

  .dark {
    right: 17px;
  }
}

@media screen and (max-width: 661px) {
  p {
    display: none;
  }
}
</style>
