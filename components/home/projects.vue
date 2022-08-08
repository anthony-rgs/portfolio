<template>
  <section>
    <h2>Projets</h2>
    <div class="project-container">
      <img
        :src="projects[projectNumber].image"
        alt="L'Atelier Image"
        v-bind:class="{ active: isActive }"
      />
      <div class="bar"></div>
      <div class="text-container" v-bind:class="{ active: isActive }">
        <p>{{ projects[projectNumber].text }}</p>
        <a class="link" :href="projects[projectNumber].link">Voir le projet.</a>
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
      projects: [
        {
          image: "/projects/latelier12/latelier12-main.webp",
          text: "Premier projet professionnel qui consistait à la conception et réalisation d’un site vitrine pour un salon de coiffure. ",
          link: "/projects/latelier12",
        },
        {
          image: "/projects/pokemon/pokemon-main.webp",
          text: "Site permettant de rechercher des cartes Pokémon et d'obtenir des informations sur ces dernières grâce à des requètes API avec Axios.",
          link: "/projects/pokemon",
        },
        {
          image: "/projects/journey/journey-main.webp",
          text: "Progressive Web App qui propose de nombreux parcours qui mettent en avant les commercants et les endroits atypiques autour d'un monument. Ce projet scolaire est une preuve de concept.",
          link: "/projects/journey",
        },
        {
          image: "/projects/wanned/wanned-main.webp",
          text: "RPG réalisé dans le cadre d'un projet scolaire. Suivez l'aventure de Baptiste à travers les sous-sols de l’école pour découvrir la raison d'une mystérieuse panne.",
          link: "/projects/wanned",
        },
        {
          image: "/projects/reseau-social-main.webp",
          text: "Projet scolaire en back. Le but était de réaliser un réseau social avec de nombreuses fonctionnalités.",
          link: "/projects/reseau-social",
        },
        {
          image: "/projects/openfoodfacts/openfoodfacts-main.webp",
          text: "Refonte du site Open Food Facts. L'objectif de ce projet scolaire était de nous apprendre à utiliser Figma et de rendre le site plus intuitif, moderne et épuré.",
          link: "/projects/open-food-facts",
        },
        {
          image: "/projects/colladraw/colladraw-main.webp",
          text: "Issu d'un projet scolaire, Colladraw est un 'Paint' collaboratif en ligne où vous pouvez dessiner avec vos amis sur la même toile.",
          link: "/projects/colladraw",
        },
        {
          image: "/projects/mastermind/mastermind-main.webp",
          text: " Mastermind sur 10 manches avec lecteur de musique, réalisé lors de mon premier projet scolaire en Front.",
          link: "/projects/mastermind",
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
section {
  margin-top: 160px;
}

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
  /* background-color: blueviolet; */
  padding: 0 20px;
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
</style>
