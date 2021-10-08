<template>
  <main>
    <h1>Новости</h1>
    <div>
      <div class="article-block" v-for="(article, index) in news" :key="index">
        <h2>
          <router-link :to="'/article/' + article.id">{{
            article.name
          }}</router-link>
        </h2>
        <p>Опубликовано: {{ article.date }}</p>
        <p>{{ article.shortDesc }}</p>
      </div>
    </div>
  </main>
</template>

<script>
import news from "../assets/articles.json";

export default {
  name: "News",
  data() {
    return {
      news,
    };
  },
};
</script>

<style scoped>
.article-block {
  margin: 25px;
  padding: 4px;
  background-color: #ffacc5;
}

.article-block p {
  color: #ff5588;
}

a {
  color: #fff;
  text-decoration: none;
}
a:hover {
  text-decoration: underline;
}
</style>