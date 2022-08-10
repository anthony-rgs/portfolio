<template>
  <section>
    <ProjectsProjectPresentation
      :title="this.title"
      :date="this.date"
      :image="this.image"
    />
    <About> {{ about }} </About>
    <div class="buttons-container">
      <ButtonsLink
        class="first-button"
        :text="this.githubText"
        :link="this.githubLink"
      />
      <ButtonsLink :text="this.siteText" :link="this.siteLink" />
    </div>
    <div class="section role-techs">
      <ProjectsRole :text="this.role" />
      <ProjectsTechs :title="this.techsTitle" :text="this.techsText" />
    </div>
    <ProjectsGallery :images="this.gallery" />
  </section>
</template>

<script>
export default {
  data() {
    return {
      title: "POKÉMON",
      date: "Juin - 2022",
      image: "/projects/pokemon/pokemon-main.webp",
      about:
        "Site permettant de rechercher des cartes Pokémon et d'obtenir des informations sur ces dernières grâce à des requètes API avec Axios.",
      githubText: "Voir le code.",
      githubLink: "https://github.com/anthony-rgs/pokemon-cards",
      siteText: "Voir le site.",
      siteLink: "https://pokemon.anth.ooo",
      role: "Développeur",
      techsTitle: "Langages",
      techsText: "HTML - CSS - Vue.js",
      gallery: [
        { url: "/projects/pokemon/pokemon-1.webp" },
        { url: "/projects/pokemon/pokemon-2.webp" },
      ],
    };
  },

  created() {
    if (process.browser) {
      window.parent.document.title = "Anthony Ringressi - Pokémon";
    }
  },
};
</script>

<style>
* {
  --color: #3a86ff;
}
.date {
  top: 550px;
  right: 810px;
}

@media screen and (max-width: 1140px) {
  .date {
    top: 505px;
    right: 720px;
  }
}

@media screen and (max-width: 1025px) {
  .date {
    top: 494px;
    right: 710px;
  }
}
</style>
