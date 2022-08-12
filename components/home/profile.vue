<template>
  <div class="container-profile">
    <div class="profile-informations">
      <div class="name">
        <p class="title">{{ name }}</p>
        <p class="title">{{ surname }}</p>
      </div>
      <img src="~assets/images/picture-me.webp" />
    </div>
    <div class="bar"></div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      name: "Anthony",
      surname: "Ringressi",
    };
  },
};
</script>

<style scoped>
.profile-informations {
  display: flex;
  justify-content: space-between;
}

.name {
  align-self: flex-end;
}

.title:nth-child(1) {
  margin-bottom: -20px;
}

.title:nth-child(2) {
  margin: 0 0 -30px 62px;
}

img {
  height: 500px;
}

.bar {
  width: calc(100% + 120px);
  margin: 160px -120px 0;
  height: 3px;
}

@media screen and (min-width: 1700px) {
  img {
    height: 700px;
  }

  .bar {
    height: 5px;
    margin-top: 200px;
  }

  .title:nth-child(2) {
    margin: 0 0 -25px 70px;
  }
}

@media screen and (max-width: 1260px) {
  .title {
    font-size: 4.5rem;
  }

  .title:nth-child(2) {
    margin: 0 0 -29px 43px;
  }

  img {
    height: 440px;
  }

  .bar {
    width: calc(100% + 100px);

    margin: 100px -100px 0;
  }
}

@media screen and (max-width: 1000px) {
  .title {
    font-size: 3rem;
  }

  .title:nth-child(2) {
    margin: 0 0 -19px 29px;
  }

  img {
    height: 270px;
  }

  .bar {
    width: calc(100% + 100px);
    margin: 100px -100px 0;
  }
}

@media screen and (max-width: 660px) {
  .title {
    font-size: 2rem;
  }

  .title:nth-child(1) {
    margin-bottom: -5px;
  }

  .title:nth-child(2) {
    margin: 0 0 -12px 29px;
  }

  img {
    height: 240px;
  }

  .bar {
    display: none;
  }
}

@media screen and (max-width: 450px) {
  .title {
    font-size: 1.8rem;
  }

  .title:nth-child(2) {
    margin: 0 0 -11px;
  }

  img {
    height: 180px;
  }
}

@media screen and (max-width: 345px) {
  .title {
    font-size: 1.7rem;
  }

  img {
    height: 140px;
  }
}

@media screen and (max-width: 308px) {
  .title {
    font-size: 1.5rem;
  }

  .title:nth-child(2) {
    margin: 0 0 -9px;
  }

  img {
    height: 120px;
  }
}
</style>
