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
      title: "MAGGLE",
      date: "Mai - 2022",
      image: "/projects/maggle/maggle-main.webp",
      about:
        "Projet scolaire en back. Le but était de réaliser un réseau social avec de nombreuses fonctionnalités.",
      githubText: "Voir le code.",
      githubLink: "https://github.com/clementpnn/reseaux_php",
      role: "Développeur & Designer",
      techsTitle: "Langages & Outil",
      techsText: "JS - MySQL - PHP - Figma",
      gallery: [
        { url: "/projects/maggle/maggle-1.webp" },
        { url: "/projects/maggle/maggle-2.webp" },
        { url: "/projects/maggle/maggle-3.webp" },
        { url: "/projects/maggle/maggle-4.webp" },
      ],
    };
  },

  created() {
    if (process.browser) {
      window.parent.document.title = "Anthony Ringressi - Maggle";
    }
  },
};
</script>

<style>
* {
  --color: #be3443;
}

.date {
  margin-top: 287px;
  padding-top: 100px;
}
</style>
