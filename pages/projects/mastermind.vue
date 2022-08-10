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
      title: "MASTERMIND",
      date: "Février - 2022",
      image: "/projects/mastermind/mastermind-main.webp",
      about:
        "Mastermind sur 10 manches avec lecteur de musique, réalisé lors de mon premier projet scolaire en Front.",
      githubText: "Voir le code.",
      githubLink: "https://github.com/anthony-rgs/mastermind",
      siteText: "Voir le site.",
      siteLink: "https://mastermind.anth.ooo",
      role: "Développeur",
      techsTitle: "Langages",
      techsText: "HTML - CSS - JS",
      gallery: [
        { url: "/projects/mastermind/mastermind-1.webp" },
        { url: "/projects/mastermind/mastermind-2.webp" },
        { url: "/projects/mastermind/mastermind-3.webp" },
        { url: "/projects/mastermind/mastermind-4.webp" },
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

<style>
* {
  --color: #f0330a;
}

.date {
  top: 527px;
  right: 800px;
}

@media screen and (max-width: 1140px) {
  .date {
    top: 487px;
    right: 715px;
  }
}

@media screen and (max-width: 1025px) {
  .date {
    top: 477px;
    right: 700px;
  }
}
</style>
