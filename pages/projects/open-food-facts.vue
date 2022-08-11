<template>
  <section>
    <ProjectsProjectPresentation
      :title="this.title"
      :date="this.date"
      :image="this.image"
    />
    <About :text="this.about"></About>

    <ButtonsLink :text="this.siteText" :link="this.siteLink" />
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
      title: "OPEN FOOD FACTS",
      date: "Mai - 2022",
      image: "/projects/openfoodfacts/openfoodfacts-main.webp",
      about:
        "Refonte côté design du site de Open Food Facts réalisée en 1 semaine lors d'un projet scolaire en équipe. <br> <br> L'objectif de ce projet était d'approfondir nos connaissances avec l'utilisation de Figma et de rendre le site plus intuitif, moderne et épuré. <br> <br> Nous devions travailler seulement sur la page d'accueil et la page produit.",
      siteText: "Voir la maquette.",
      siteLink:
        "https://www.figma.com/file/kSdPNBV8rToXUqsNP66wqJ/Projet?node-id=1%3A4",
      role: "Designer",
      techsTitle: "Outils",
      techsText: "Figma - Photoshop",
      gallery: [
        { url: "/projects/openfoodfacts/openfoodfacts-1.webp" },
        { url: "/projects/openfoodfacts/openfoodfacts-2.webp" },
        { url: "/projects/openfoodfacts/openfoodfacts-3.webp" },
        { url: "/projects/openfoodfacts/openfoodfacts-4.webp" },
      ],
    };
  },

  created() {
    if (process.browser) {
      window.parent.document.title = "Anthony Ringressi - Open Food Facts";
    }
  },
};
</script>

<style>
* {
  --color: #47ae7a;
}

.date {
  top: 557px;
  right: 820px;
}

@media screen and (max-width: 1140px) {
  .date {
    top: 500px;
    right: 735px;
  }
}

@media screen and (max-width: 1025px) {
  .date {
    top: 480px;
    right: 715px;
  }
}
</style>
