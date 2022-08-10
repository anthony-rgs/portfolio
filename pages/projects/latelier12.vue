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
      title: "L'ATELIER 12",
      date: "Mai - 2022",
      image: "/projects/latelier12/latelier12-main.webp",
      about:
        "Premier projet professionnel qui consistait à la conception et réalisation d’un site vitrine pour un salon de coiffure situé dans le 5ème arrondissement de Paris.",
      githubText: "Voir le code.",
      githubLink: "https://github.com/anthony-rgs/atelier12-frontend",
      siteText: "Voir le site.",
      siteLink: "https://latelier12.fr",
      role: "Designer & Développeur",
      techsTitle: "Langages & Outil",
      techsText: "HTML - CSS - JS - Figma",
      gallery: [
        { url: "/projects/latelier12/latelier12-1.webp" },
        { url: "/projects/latelier12/latelier12-2.webp" },
        { url: "/projects/latelier12/latelier12-3.webp" },
        { url: "/projects/latelier12/latelier12-4.webp" },
      ],
    };
  },

  created() {
    if (process.browser) {
      window.parent.document.title = "Anthony Ringressi - L'Atelier 12";
    }
  },
};
</script>

<style>
* {
  --color: #5c61da;
}

.date {
  top: 557px;
  right: 820px;
}

@media screen and (max-width: 1140px) {
  .date {
    top: 510px;
    right: 735px;
  }
}

@media screen and (max-width: 1025px) {
  .date {
    top: 500px;
    right: 715px;
  }
}
</style>
