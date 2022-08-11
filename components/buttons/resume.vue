<template>
  <a class="link" :href="resumeLink" download>{{ text }}</a>
</template>

<script>
export default {
  data() {
    return {
      text: "Télécharger mon cv.",
      resumeLink: "/cv-ringressi-anthony.pdf",
    };
  },
};
</script>
