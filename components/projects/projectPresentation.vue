<template>
  <section class="project-resentation-container">
    <a href="/" class="title">{{ title }}</a>
    <div>
      <p class="date">{{ date }}</p>
      <img :src="image" alt="Project picture" />
    </div>
  </section>
</template>

<script>
export default {
  props: {
    title: String,
    date: String,
    image: String,
  },
};
</script>

<style>
.project-resentation-container {
  margin-top: -80px;
}

.project-resentation-container div {
  margin-top: 80px;
  display: flex;
  justify-content: flex-end;
}

.date {
  transform: rotate(-90deg);
  height: 35px;
}

.project-resentation-container img {
  width: 750px;
  height: 428px;
}
</style>
