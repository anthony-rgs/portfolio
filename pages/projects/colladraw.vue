<template>
  <section>
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
      title: "COLLADRAW",
      date: "Mars - 2022",
      image: "/projects/colladraw/colladraw-main.webp",
      about:
        "Colladraw est une application de dessin en ligne réalisée en 1 semaine dans le cadre d'un projet full-stack en équipe. <br> <br> En plus de pouvoir dessiner, Colladraw propose une collaboration en temps réel et la création de compte pour sauvegarder ses dessins automatiquement dans le cloud.",
      githubText: "Voir le code.",
      githubLink: "https://github.com/baptistedph/colladraw",
      siteText: "Voir le site.",
      siteLink: "https://colladraw.fun",
      role: "Designer & Développeur",
      techsTitle: "Langages & Outil",
      techsText: "JS - Laravel - MySQL - Figma",
      gallery: [
        "/projects/colladraw/colladraw-1.webp",
        "/projects/colladraw/colladraw-2.webp",
        "/projects/colladraw/colladraw-3.webp",
        "/projects/colladraw/colladraw-4.webp",
      ],
    };
  },

  created() {
    if (process.browser) {
      window.parent.document.title = "Anthony Ringressi - Colladraw";
    }
  },
};
</script>

<style scoped>
* {
  --color: #9c92e1;
}
</style>

<style>
.date {
  top: 609px;
  right: 810px;
}

@media screen and (min-width: 1700px) {
  .date {
    top: 927px;
    right: 1245px;
  }
}

@media screen and (max-width: 1140px) {
  .date {
    top: 564px;
    right: 720px;
  }
}

@media screen and (max-width: 1025px) {
  .date {
    top: 574px;
    right: 700px;
  }
}
</style>
