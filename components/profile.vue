<template>
  <div class="container-profile">
    <div class="profile-informations">
      <div class="name">
        <p class="title">Anthony</p>
        <p class="title">Ringressi</p>
      </div>

      <img src="~assets/images/picture-me.webp" />
    </div>
    <div class="bar"></div>
  </div>
</template>

<script></script>

<style scoped>
.profile-informations {
  display: flex;
  justify-content: space-between;
}

.name {
  align-self: flex-end;
}

.title:nth-child(2) {
  margin: 0 0 -40px 62px;
}

img {
  height: 500px;
}

.bar {
  width: calc(100% + 120px);
  margin: 160px -120px 0;
  height: 3px;
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
  .profile-informations {
    flex-direction: column-reverse;
  }

  /* .title:nth-child(1) {
    margin-top: 10px;
  } */

  .title:nth-child(2) {
    margin: 0;
  }

  .name {
    align-self: flex-start;
  }

  img {
    width: 180px;
    height: 100%;
  }
}
</style>
