<template>
  <section>
    <ButtonsBack />
    <ProjectsProjectPresentation
      :title="this.title"
      :date="this.date"
      :image="this.image"
    />
    <About :text="this.about"> </About>
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
        "Dans le cadre d'un projet scolaire de une semaine en équipe, nous avons eu pour consigne de faire un réseau social en back. <br> <br> Ce projet contient de nombreuses fonctionnalités comme la possibilitée de créer un compte, de se déconnecter, d'écrire des posts, de modifier toutes les informations de son profil, de rechercher et d'ajouter des amis, des groupes ou des pages. ",
      githubText: "Voir le code.",
      githubLink: "https://github.com/clementpnn/reseaux_php",
      role: "Développeur & Designer",
      techsTitle: "Langages & Outil",
      techsText: "JS - MySQL - PHP - Figma",
      gallery: [
        "/projects/maggle/maggle-1.webp",
        "/projects/maggle/maggle-2.webp",
        "/projects/maggle/maggle-3.webp",
        "/projects/maggle/maggle-4.webp",
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

<style scoped>
* {
  --color: #be3443;
}
</style>

<style>
.date {
  top: 616px;
  right: 820px;
}

@media screen and (min-width: 1700px) {
  .date {
    top: 939px;
    right: 1245px;
  }
}

@media screen and (max-width: 1140px) {
  .date {
    top: 571px;
    right: 735px;
  }
}

@media screen and (max-width: 1025px) {
  .date {
    top: 580px;
    right: 715px;
  }
}
</style>
