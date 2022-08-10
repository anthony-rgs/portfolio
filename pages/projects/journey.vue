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
      title: "JOURNEY",
      date: "Juin - 2022",
      image: "/projects/journey/journey-main.webp",
      about:
        "Progressive Web App qui propose de nombreux parcours qui mettent en avant les commercants et les endroits atypiques autour d'un monument. Ce projet scolaire est une preuve de concept.",
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
