<template>
  <div id="app">
    <div id="nav">
      <Header />
    </div>
    <div class="content">
      <router-view />
    </div>
  </div>
</template>

<script>
import Header from "@/components/Header.vue";

export default {
  name: "App",
  components: {
    Header,
  },
};

document.title = "Лабораторная работа №1";
</script>

<style>
html,
body {
  width: 100%;
  height: 100%;
  padding: 0;
  margin: 0;
  background-color: #ff94b4;
  color: #fff;
  font-family: Arial, "Helvetica Neue", Helvetica, sans-serif;
}

#app {
  position: relative;
  text-align: center;
  min-height: 100%;
}

.content {
  flex: 1 1 auto;
  margin: 0 20%;
}
</style>
