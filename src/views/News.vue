<template>
  <div id="app">
    <News />
  </div>
</template>

<script>
import News from "@/components/News.vue";

export default {
  name: "NewsPage",
  components: {
    News,
  },
};
</script>

<style>
body {
  font-family: Arial, Helvetica, sans-serif;
}
</style>
