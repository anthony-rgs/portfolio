<template>
  <div class="container-profile">
    <div class="profile-informations">
      <div class="name">
        <h1>
          Anthony <br />
          <span>Ringressi</span>
        </h1>
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

span {
  margin: 40px 0 -10px 62px;
}

img {
  height: 500px;
}

.bar {
  width: calc(100% + 120px);
  margin: 160px -120px 0;
  height: 3px;
}
</style>
