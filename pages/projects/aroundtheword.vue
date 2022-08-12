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
      title: "AROUND THE WORD",
      date: "Novembre - 2021",
      image: "/projects/aroundtheword/aroundtheword-main.webp",
      about:
        "Around The Word est mon tout premier projet. Cela faisait à peine un mois que j'avais appris la programmation. <br> <br> La consigne était de réaliser un simple Scrabble sur le terminal. J'y ai ajouté de nombreuses fonctionnalités afin de rendre l'affichage et le jeu plus intéressant. <br> <br> Par exemple il y a 37 listes de mots pour 1688 mots différents, un magasin pour acheter des bonus et autre, mais aussi un mode de jeu caché où toutes erreurs conduira à la fin de votre partie ! Bien entendu le jeu est compatible sur Windows et Mac. <br> <br> Le but du jeu est de trouver les 3 mots cachés de la manche. Une partie se déroule en 3 manches. À chaque bonne réponse vous gagnez des points et du cash. Servez-vous en pour acheter des bonus dans le magasin ou en partie. Arriverez-vous à sortir victorieux de Around the Word ?",
      githubText: "Voir le code.",
      githubLink: "https://github.com/anthony-rgs/scrabble",
      role: "Développeur",
      techsTitle: "Langage",
      techsText: "Python",
      gallery: [
        { url: "/projects/aroundtheword/aroundtheword-1.webp" },
        { url: "/projects/aroundtheword/aroundtheword-2.webp" },
        { url: "/projects/aroundtheword/aroundtheword-3.webp" },
        { url: "/projects/aroundtheword/aroundtheword-4.webp" },
        { url: "/projects/aroundtheword/aroundtheword-5.webp" },
        { url: "/projects/aroundtheword/aroundtheword-6.webp" },
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
  --color: #fff;
}

.bg-light * {
  --color: #000;
}

.date {
  top: 519px;
  right: 790px;
}

@media screen and (min-width: 1700px) {
  .date {
    top: 801px;
    right: 1200px;
  }
}
@media screen and (max-width: 1140px) {
  .date {
    top: 480px;
    right: 705px;
  }
}

@media screen and (max-width: 1025px) {
  .date {
    top: 470px;
    right: 680px;
  }
}
</style>
