<template>
  <a class="link" :href="link" target="blank"> {{ text }}</a>
</template>

<script>
export default {
  props: {
    link: String,
    text: String,
  },
};
</script>
