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
      title: "COLLADRAW",
      date: "March - 2022",
      image: "/projects/colladraw/colladraw-main.webp",
      about:
        "Issu d'un projet scolaire, Colladraw est un 'Paint' collaboratif en ligne où vous pouvez dessiner avec vos amis sur la même toile.",
      githubText: "Voir le code.",
      githubLink: "https://github.com/baptistedph/colladraw",
      siteText: "Voir le site.",
      siteLink: "https://colladraw.fun",
      role: "Designer & Développeur",
      techsTitle: "Langages & Outils",
      techsText: "JS - Laravel - MySQL - Figma",
      gallery: [
        { url: "/projects/colladraw/colladraw-1.webp" },
        { url: "/projects/colladraw/colladraw-2.webp" },
        { url: "/projects/colladraw/colladraw-3.webp" },
        { url: "/projects/colladraw/colladraw-4.webp" },
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

<style>
* {
  --color: #9c92e1;
}

.date {
  top: 542px;
  right: 810px;
}

@media screen and (max-width: 1140px) {
  .date {
    top: 500px;
    right: 720px;
  }
}

@media screen and (max-width: 1025px) {
  .date {
    top: 488px;
    right: 700px;
  }
}
</style>
