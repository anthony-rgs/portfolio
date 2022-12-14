<template>
  <section class="section">
    <ImagesLoader :images="this.images" />

    <h2>{{ title }}</h2>
    <div class="project-container">
      <img
        :src="projects[projectNumber].image"
        alt="Image"
        v-bind:class="{ active: isActive }"
        rel="preload"
      />
      <div class="bar"></div>
      <div class="text-container" v-bind:class="{ active: isActive }">
        <p>{{ projects[projectNumber].text }}</p>
        <NuxtLink class="link" :to="projects[projectNumber].link">{{
          buttonText
        }}</NuxtLink>
      </div>
    </div>
    <div class="switch-project">
      <div class="before" @click="before">
        <div class="switch horizontal"></div>
      </div>
      <div class="after" @click="after">
        <div class="switch"></div>
        <div class="switch horizontal"></div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  data() {
    return {
      projectNumber: 0,
      isActive: true,
      title: "Projets",
      buttonText: "En savoir plus.",
      images: [
        "/projects/latelier12/latelier12-main.webp",
        "/projects/pokemon/pokemon-main.webp",
        "/projects/journey/journey-main.webp",
        "/projects/wanned/wanned-main.webp",
        "/projects/maggle/maggle-main.webp",
        "/projects/openfoodfacts/openfoodfacts-main.webp",
        "/projects/colladraw/colladraw-main.webp",
        "/projects/mastermind/mastermind-main.webp",
        "/projects/aroundtheword/aroundtheword-main.webp",
      ],
      projects: [
        {
          image: "/projects/latelier12/latelier12-main.webp",
          text: "Lors de mon premier projet professionnel, j'ai travaillé sur la conception et la réalisation d’un site vitrine pour un salon de coiffure.",
          link: "/projects/latelier12",
        },
        {
          image: "/projects/pokemon/pokemon-main.webp",
          text: "Site permettant de rechercher des cartes Pokémon et d'obtenir des informations sur ces dernières grâce à des requètes API avec Axios.",
          link: "/projects/pokemon",
        },
        {
          image: "/projects/journey/journey-main.webp",
          text: "Progressive Web App qui propose de nombreux parcours qui mettent en avant les commercants et les endroits atypiques autour d'un monument.",
          link: "/projects/journey",
        },
        {
          image: "/projects/maggle/maggle-main.webp",
          text: "Projet scolaire en back. Le but était de réaliser un réseau social avec de nombreuses fonctionnalités.",
          link: "/projects/maggle",
        },
        {
          image: "/projects/openfoodfacts/openfoodfacts-main.webp",
          text: "L'objectif de ce projet scolaire était de nous apprendre à utiliser Figma en effectuant la refonte du site Open Food Facts. ",
          link: "/projects/open-food-facts",
        },
        {
          image: "/projects/wanned/wanned-main.webp",
          text: "RPG réalisé dans le cadre d'un projet scolaire. Plusieurs épreuves sont à relever comme des énigmes ou des combats. ",
          link: "/projects/wanned",
        },
        {
          image: "/projects/colladraw/colladraw-main.webp",
          text: "Issu d'un projet scolaire, Colladraw est un 'Paint' collaboratif en ligne où vous pouvez dessiner avec vos amis sur la même toile.",
          link: "/projects/colladraw",
        },
        {
          image: "/projects/mastermind/mastermind-main.webp",
          text: "Mastermind sur 10 manches avec lecteur de musique, réalisé lors de mon premier projet scolaire en Front.",
          link: "/projects/mastermind",
        },
        {
          image: "/projects/aroundtheword/aroundtheword-main.webp",
          text: "Pour mon tout premier projet dev, j'ai réalisé un Scrabble sur le terminal avec de nombreuses fonctionnalités.",
          link: "/projects/aroundtheword",
        },
      ],
    };
  },

  methods: {
    before() {
      this.isActive = false;
      setTimeout(() => {
        let length = this.projects.length;
        if (this.projectNumber == 0) {
          this.projectNumber = length - 1;
        } else {
          this.projectNumber--;
        }
        this.isActive = true;
      });
    },

    after() {
      this.isActive = false;
      setTimeout(() => {
        if (this.projects.length - 1 == this.projectNumber) {
          this.projectNumber = 0;
        } else {
          this.projectNumber++;
        }
        this.isActive = true;
      });
    },
  },
};
</script>

<style scoped>
.project-container {
  display: flex;
  justify-content: space-between;
}

img {
  width: 575px;
  height: 100%;
  opacity: 0;
}

.bar {
  height: 328px;
  width: 3px;
}

.text-container {
  width: 500px;
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  opacity: 0;
}

a {
  width: fit-content;
}

.switch-project {
  display: flex;
  justify-content: space-around;
  margin-top: 80px;
}

.after {
  display: flex;
}

.after,
.before {
  padding: 0 20px;
  cursor: pointer;
}

.switch {
  width: 3px;
  height: 40px;
  background-color: var(--color);
}

.horizontal {
  transform: rotate(90deg);
  position: absolute;
}

.active {
  opacity: 1;
  transition: opacity 0.4s ease;
}

@media screen and (min-width: 1700px) {
  img,
  .text-container {
    width: 48%;
  }

  .bar {
    display: none;
  }

  .switch-project {
    margin-top: 160px;
  }

  .switch {
    height: 60px;
    width: 5px;
  }

  .after,
  .before {
    padding: 0 30px;
  }
}

@media screen and (max-width: 1370px) {
  img {
    width: 500px;
  }

  .bar {
    height: 285px;
  }
}

@media screen and (max-width: 1270px) {
  img {
    width: 400px;
  }

  .bar {
    height: 229px;
  }

  .text-container {
    width: 350px;
  }

  p {
    font-size: 20px;
  }
}

@media screen and (max-width: 1000px) {
  img {
    width: 100%;
  }

  .bar {
    display: none;
  }

  .text-container {
    width: 100%;
    margin-top: 30px;
  }

  .link {
    margin-top: 30px;
  }

  p {
    font-size: 16px;
  }

  .project-container {
    display: block;
  }

  .switch-project {
    margin-top: 50px;
  }
}

@media screen and (max-width: 660px) {
  .text-container,
  .link {
    margin-top: 20px;
  }

  .switch-project {
    margin-top: 40px;
  }

  .switch {
    height: 30px;
  }

  .after,
  .before {
    padding: 0 15px;
  }
}
</style>
