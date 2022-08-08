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
      <ProjectsTechs :text="this.techs" />
    </div>
    <ProjectsGallery :images="this.gallery" />
  </section>
</template>

<script>
export default {
  data() {
    return {
      title: "Journey",
      date: "Juin - 2022",
      image: "/projects/journey/journey-main.webp",
      about:
        "Progressive Web App qui propose de nombreux parcours qui mettent en avant les commercants et les endroits atypiques autour d'un monument. Ce projet scolaire est une preuve de concept.",
      githubText: "Voir le code",
      githubLink: "https://github.com/Leambr/Journey",
      siteText: "Voir le site",
      siteLink: "https://journey.anth.ooo",
      role: "Designer & Développeur",
      techs: "React - PHP - Figma",
      gallery: [
        { url: "/projects/journey/journey-1.webp" },
        { url: "/projects/journey/journey-2.webp" },
        { url: "/projects/journey/journey-3.webp" },
      ],
    };
  },
};
</script>

<style>
* {
  --color: #ffb800;
}

.date {
  margin-top: 276px;
  padding-top: 110px;
}
</style>
