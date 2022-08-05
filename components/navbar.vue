<template>
  <div class="nav">
    <div @click="active" class="button" :class="{ active: isActive }">
      <div></div>
      <div></div>
      <div></div>
    </div>

    <div v-show="isActive === true" class="nav-categories">
      <ul>
        <li v-for="language in languages" :key="language">{{ language }}</li>
      </ul>
      <SwitchMode />
    </div>
  </div>
</template>

<script>
import switchMode from "./switchMode.vue";
export default {
  components: { switchMode },
  data() {
    return {
      isActive: false,
      languages: ["Français", "English", "Español", "Latin"],
    };
  },
  methods: {
    active() {
      this.isActive = !this.isActive;
    },
  },
};
</script>

<style scoped>
.nav {
  position: fixed;
  right: 27px;
  top: 50px;
}

.button div {
  height: 3px;
  margin-bottom: 5px;
  background-color: var(--blue);
  transition: all 0.3s ease-in-out;
}

.button div:nth-child(1) {
  width: 62px;
}

.button div:nth-child(2) {
  width: 45px;
}

.button div:nth-child(3) {
  width: 30px;
}

.active div:nth-child(2) {
  margin-bottom: -3px;
  width: 50px;
}

li {
  font-size: 0.813rem;
}

li:nth-child(1) {
  margin: 54px 0 40px 0;
}

li:nth-child(2) {
  margin-bottom: 40px;
}

li:nth-child(4) {
  margin: 40px 0 304px;
}

ul.active,
p.active {
  animation: showup 0.7s;
}

@keyframes showup {
  0% {
    opacity: 0;
  }
  100% {
    opacity: 1;
  }
}
</style>
