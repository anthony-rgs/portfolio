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
      title: "L'ATELIER 12",
      date: "Mai - 2022",
      image: "/projects/latelier12/latelier12-main.webp",
      about:
        "Pour mon premier projet professionnel j'ai eu l'opportunité de travailler sur la conception et la réalisation d’un site vitrine pour un salon de coiffure, situé dans le 5ème arrondissement de Paris. <br> <br> La cliente avait besoin d’un site vitrine avec les tarifs, les infos pratiques et les informations des produits qu’elle vend dans son salon. <br> <br> Elle voulait que le site soit moderne et épuré.",
      githubText: "Voir le code.",
      githubLink: "https://github.com/anthony-rgs/atelier12-frontend",
      siteText: "Voir le site.",
      siteLink: "https://latelier12.fr",
      role: "Designer & Développeur",
      techsTitle: "Langages & Outil",
      techsText: "HTML - CSS - JS - Figma",
      gallery: [
        "/projects/latelier12/latelier12-1.webp",
        "/projects/latelier12/latelier12-2.webp",
        "/projects/latelier12/latelier12-3.webp",
        "/projects/latelier12/latelier12-4.webp",
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
  top: 556px;
  right: 820px;
}

@media screen and (min-width: 1700px) {
  .date {
    top: 856px;
    right: 1245px;
  }
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
