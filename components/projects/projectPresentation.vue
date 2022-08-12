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

.title {
  font-size: 5rem;
}

.project-resentation-container div {
  margin-top: 80px;
  display: flex;
  justify-content: flex-end;
}

.date {
  transform: rotate(-90deg);
  position: absolute;
}

.project-resentation-container img {
  width: 750px;
  height: 428px;
}

@media screen and (min-width: 1700px) {
  .project-resentation-container {
    margin-top: -62px;
  }

  .project-resentation-container img {
    width: 1200px;
    height: 690px;
  }

  .title {
    font-size: 120px;
  }
}

@media screen and (max-width: 1140px) {
  .project-resentation-container {
    margin-top: -70px;
  }

  .title {
    font-size: 4rem;
  }

  .project-resentation-container img {
    width: 650px;
    height: 374px;
  }

  p {
    font-size: 1.26rem;
  }
}

@media screen and (max-width: 1025px) {
  .project-resentation-container {
    margin-top: -60px;
  }
}

@media screen and (max-width: 885px) {
  .project-resentation-container {
    margin-top: -30px;
  }

  .title {
    font-size: 3rem;
  }

  .project-resentation-container div {
    margin-top: 60px;
    flex-direction: column-reverse;
  }

  .project-resentation-container img {
    width: 100%;
    height: 100%;
  }

  .date {
    transform: rotate(0);
    position: initial;
  }
}

@media screen and (max-width: 661px) {
  .title {
    font-size: 2rem;
  }

  .project-resentation-container div {
    margin-top: 40px;
  }

  .project-resentation-container {
    margin-top: 0px;
  }
}
</style>
