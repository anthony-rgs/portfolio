<template>
  <section>
    <h2>Contact</h2>
    <div class="contact">
      <p>
        Si vous avez une question ou une remarque n’hésitez pas à me contacter
        par mail ou via mes réseaux sociaux.
      </p>
      <div class="links-container">
        <a href="https://www.linkedin.com/in/anthony-ringressi/" target="blank">
          <img src="~assets/icons/linkedin.svg" alt="Linkedin icon" />
          <p>Anthony Ringressi</p>
        </a>
        <a href="mailto::contact@anth.ooo?subject=Coucou :)" target="blank">
          <img src="~assets/icons/mail.svg" alt="Mail icon" />
          <p>contact@anth.ooo</p>
        </a>
        <a href="https://github.com/anthony-rgs" target="blank">
          <img src="~assets/icons/github.svg" alt="Github icon" />
          <p>anthony-rgs</p>
        </a>
      </div>
    </div>
  </section>
</template>

<script>
export default {};
</script>

<style scoped>
section {
  margin-top: 160px;
}

p:nth-child(1) {
  width: 460px;
}

.contact {
  display: flex;
  justify-content: space-between;
}

.links-container {
  display: flex;
  flex-direction: column;
  justify-content: space-between;
}

.links-container a {
  display: flex;
  padding: 0;
}

.links-container img {
  margin-right: 30px;
}

@media screen and (max-width: 1025px) {
  section {
    margin-top: 120px;
  }

  p:nth-child(1) {
    width: 360px;
  }

  .links-container img {
    margin-right: 20px;
  }
}

@media screen and (max-width: 850px) {
  p:nth-child(1) {
    width: 280px;
  }

  .links-container img {
    margin-right: 20px;
    width: 20px;
  }
}

@media screen and (max-width: 660px) {
  section {
    margin-top: 100px;
  }

  .contact {
    display: block;
  }

  p:nth-child(1) {
    width: 100%;
  }

  .links-container img {
    margin-right: 20px;
    width: 15px;
  }

  .links-container a {
    margin-top: 20px;
  }
}
</style>
