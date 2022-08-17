<template>
  <section class="project-section">
    <ButtonsBack />
    <ProjectsProjectPresentation
      :title="this.title"
      :date="this.date"
      :image="this.image"
    />
    <About :text="this.about"> </About>
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
      title: "WANNED",
      date: "Avril - 2022",
      image: "/projects/wanned/wanned-main.webp",
      about:
        "RPG réalisé en deux semaines dans le cadre d'un projet front en équipe. <br> <br> À l’école du web, HETIC, la Wifi ne fonctionne plus depuis maintenant 3 jours. Suivez l’aventure d’un valeureux guerrier nommé Baptiste, et aidez le a se frayer un chemin à travers les sous-sols de l’école pour découvrir la raison de cette mystérieuse panne... <br> </br> Les maps ont été réalisées avec Tiled et les personnages en Pixel Art avec Photshop. <br> <br> Le jeu n'est jouable que sur PC.",
      githubText: "Voir le code.",
      githubLink: "https://github.com/anthony-rgs/wanned",
      siteText: "Voir le site.",
      siteLink: "https://wanned.fun",
      role: "Développeur",
      techsTitle: "Langages",
      techsText: "HTML - CSS - JS",
      gallery: [
        "/projects/wanned/wanned-1.webp",
        "/projects/wanned/wanned-2.webp",
        "/projects/wanned/wanned-3.webp",
        "/projects/wanned/wanned-4.webp",
      ],
    };
  },

  created() {
    if (process.browser) {
      window.parent.document.title = "Anthony Ringressi - Wanned";
    }
  },
};
</script>

<style scoped>
* {
  --color: #472d3d;
}
</style>

<style>
.date {
  top: 601px;
  right: 810px;
}

@media screen and (min-width: 1700px) {
  .date {
    top: 915px;
    right: 1235px;
  }
}

@media screen and (max-width: 1140px) {
  .date {
    top: 558px;
    right: 720px;
  }
}

@media screen and (max-width: 1025px) {
  .date {
    top: 568px;
    right: 710px;
  }
}
</style>
