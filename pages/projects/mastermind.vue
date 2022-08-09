<template>
  <section>
    <ProjectsProjectPresentation
      :title="this.title"
      :date="this.date"
      :image="this.image"
    />
    <About> {{ about }} </About>
    <ButtonsLink
      class="first-button"
      :text="this.githubText"
      :link="this.githubLink"
    />
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
  margin-top: 237px;
  padding-top: 144px;
}
</style>
