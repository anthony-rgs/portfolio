<template>
  <div>
    <HomeProfile />
    <About :text="this.about"> </About>
    <ButtonsResume />
    <HomeProjects />
    <HomeSkills />
    <HomeContact />
  </div>
</template>

<script>
export default {
  data() {
    return {
      about:
        "<p> Bonjour 👋🏻 <br /> <br />J'ai 23 ans, j'habite à Paris et je suis actuellement étudiant en première année à HETIC, dans un bachelor concepteur développeur web. <br /> <br />  Plus à l'aise en Front mais ne voulant pas me limiter, je m'intéresse à tous les côtés du développement et je me donne à fond dans chacun des projets que j'entreprends, tout en essayant de faire mieux que le précédent.<br> <br> Le côté concret et l'accessibilité des ressources du web m'ont toujours intéressé. C'est pourquoi j'ai décidé de me réorienter en Octobre 2021, d'une licence d'Espagnol et études internationales à la Sorbonne. </p>",
    };
  },
};
</script>

<style>
* {
  --color: #1c58f0;
}
</style>
