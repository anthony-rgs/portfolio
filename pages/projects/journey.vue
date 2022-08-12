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
      title: "JOURNEY",
      date: "Juin - 2022",
      image: "/projects/journey/journey-main.webp",
      about:
        "Lors de notre projet final de première année, nous avons eu l'occasion de travailler en équipe sur une Progressive Web App pour la Jeune Chambre Économique de Paris. <br> <br> Nous devions trouver une solution pour donner envie aux gens d'effectuer leurs achats dans les commerces physique et non en ligne. <br> <br> Nous avons donc eu l'idée de créer une application qui propose aux touristes de nombreux parcours qui mettent en avant les commercants et les endroits atypiques autour d'un monument. Cela aurait pour objectif de mieux leur faire visiter Paris mais aussi de les inciter à consommer dans des boutiques de quartier. <br> <br> La version web explique le projet qui est disponible sur la version mobile. <br> <br> Journey est une preuve de concept.",
      githubText: "Voir le code.",
      githubLink: "https://github.com/Leambr/Journey",
      siteText: "Voir le site.",
      siteLink: "https://journey.anth.ooo",
      role: "Designer & Développeur",
      techsTitle: "Langages & Outil",
      techsText: "React - PHP - Figma",
      gallery: [
        { url: "/projects/journey/journey-1.webp" },
        { url: "/projects/journey/journey-2.webp" },
        { url: "/projects/journey/journey-3.webp" },
      ],
    };
  },

  created() {
    if (process.browser) {
      window.parent.document.title = "Anthony Ringressi - Journey";
    }
  },
};
</script>

<style>
* {
  --color: #ffb800;
}

.date {
  top: 550px;
  right: 810px;
}

@media screen and (min-width: 1700px) {
  .date {
    top: 846px;
    right: 1245px;
  }
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
