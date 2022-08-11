<template>
  <div>
    <p class="light" v-if="active === false" @click="switchMode">
      {{ mode.light }}
    </p>
    <p class="dark" v-if="active === true" @click="switchMode">
      {{ mode.dark }}
    </p>
  </div>
</template>

<script>
export default {
  data() {
    return {
      mode: { light: "Clair", dark: "Sombre" },
      active: false,
    };
  },
  methods: {
    switchMode() {
      this.active = !this.active;

      if (this.active === true) {
        document.body.classList.add("bg-light");
        if (process.client) {
          localStorage.setItem("lightMode", "true");
        }
      } else {
        document.body.classList.remove("bg-light");
        if (process.client) {
          localStorage.setItem("lightMode", "false");
        }
      }
    },
  },
  created() {
    if (process.client) {
      if (localStorage.getItem("lightMode") === null) {
        this.active = false;
      }
      if (localStorage.getItem("lightMode") === "true") {
        this.active = true;
      }
    }
  },
};
</script>

<style>
/* Light Mode */
.bg-light {
  background-color: var(--light);
  color: var(--black);
  transition: background 0.2s linear, color 0.2s linear;
}

.bg-light .bar {
  background-color: var(--dark);
}

.bg-light a {
  color: var(--black);
}

.light,
.dark {
  position: fixed;
  top: 50px;
  font-family: SCP-Regular;
  font-size: 0.813rem;
}

.light {
  right: 40px;
}

.dark {
  right: 37px;
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
  .light,
  .dark {
    display: none;
  }
}
</style>
