<template>
  <div >
    <Article v-bind:id="$route.params.id" />
  </div>
</template>

<script>
import Article from "@/components/Article.vue";
export default {
  name: "Home",
  components: {
    Article,
  },
};
</script>

<style>
</style>