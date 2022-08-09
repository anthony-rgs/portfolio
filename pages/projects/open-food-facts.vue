<template>
  <section>
    <ProjectsProjectPresentation
      :title="this.title"
      :date="this.date"
      :image="this.image"
    />
    <About> {{ about }} </About>

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
        "Refonte du site Open Food Facts. L'objectif de ce projet scolaire était de nous apprendre à utiliser Figma et de rendre le site plus intuitif, moderne et épuré.",
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
  --color: #74c69d;
}

.date {
  margin-top: 287px;
  padding-top: 100px;
}
</style>
