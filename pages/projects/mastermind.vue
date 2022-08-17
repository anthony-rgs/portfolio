<template>
  <section>
    <ButtonsBack />
    <ProjectsProjectPresentation
      :title="this.title"
      :date="this.date"
      :image="this.image"
    />
    <About :text="this.about"></About>
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
      title: "MASTERMIND",
      date: "Février - 2022",
      image: "/projects/mastermind/mastermind-main.webp",
      about:
        "Mastermind sur 10 manches, réalisé lors de mon premier projet front. <br> <br>La consigne était de réaliser un Mastermind console en JavaScript. J'ai essayé d'aller plus loin en ajoutant de nombreuses fonctionnalités comme une interface graphique (avec responsive), un light mode et surtout un lecteur musique pour animer vos parties !",
      githubText: "Voir le code.",
      githubLink: "https://github.com/anthony-rgs/mastermind",
      siteText: "Voir le site.",
      siteLink: "https://mastermind.anth.ooo",
      role: "Développeur",
      techsTitle: "Langages",
      techsText: "HTML - CSS - JS",
      gallery: [
        "/projects/mastermind/mastermind-1.webp",
        "/projects/mastermind/mastermind-2.webp",
        "/projects/mastermind/mastermind-3.webp",
        "/projects/mastermind/mastermind-4.webp",
      ],
    };
  },

  created() {
    if (process.browser) {
      window.parent.document.title = "Anthony Ringressi - Mastermind";
    }
  },
};
</script>

<style scoped>
* {
  --color: #f0330a;
}
</style>

<style>
.date {
  top: 588px;
  right: 800px;
}

@media screen and (min-width: 1700px) {
  .date {
    top: 895px;
    right: 1225px;
  }
}

@media screen and (max-width: 1140px) {
  .date {
    top: 547px;
    right: 715px;
  }
}

@media screen and (max-width: 1025px) {
  .date {
    top: 557px;
    right: 700px;
  }
}
</style>
