<template>
  <section class="section">
    <h2>{{ title }}</h2>
    <div class="contact">
      <p>{{ text }}</p>

      <div class="links-container">
        <a
          v-for="(link, indice) in links"
          :key="indice"
          :href="link[0]"
          target="blank"
        >
          <img :src="link[1]" alt="Icon" />
          <p>{{ link[2] }}</p>
        </a>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  data() {
    return {
      title: "Contact",
      text: "Si vous avez une question ou une remarque n’hésitez pas à me contacter par mail ou via mes réseaux sociaux.",

      links: [
        [
          "https://www.linkedin.com/in/anthony-ringressi/",
          "/icons/linkedin.svg",
          "Anthony Ringressi",
        ],

        ["mailto:contact@anth.ooo", "/icons/mail.svg", "contact@anth.ooo"],
        ["https://github.com/anthony-rgs", "/icons/github.svg", "anthony-rgs"],
      ],
    };
  },
};
</script>

<style scoped>
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
  align-items: center;
}

.links-container img {
  margin-right: 30px;
}

@media screen and (min-width: 1700px) {
  p:nth-child(1) {
    width: 700px;
  }

  .links-container img {
    margin-right: 50px;
    height: 40px;
  }
}

@media screen and (max-width: 1025px) {
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
  .contact {
    display: block;
  }

  p:nth-child(1) {
    width: 100%;
  }

  .links-container img {
    margin: 0 20px 0 0;
    width: 15px;
  }

  .links-container a {
    margin-top: 20px;
  }
}
</style>
