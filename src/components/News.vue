<template>
  <div class="text-center">
    <h1 class="text-h1 white--text">Новости</h1>
    <div>
    <v-container
      class="grey lighten-5 mb-6"
    >
      <v-row
        v-for="(article, i) in news" :key="i"
        align="start"
        no-gutters
        class="ma-20"
      >
        <v-col
        >
          <v-card
            class="pa-2"
            outlined
            tile
          >
            <div class="text-h5 pa-2">
                <router-link class="link" :to="'/article/' + article.id">
                <v-img class="article-img"
                  :src="require('./../assets/images/' + article.preview_image)"
                ></v-img>
                  {{article.shortDesc}}
                </router-link>
            </div>
          </v-card>
        </v-col>
      </v-row>
    </v-container>
  </div>
  </div>
</template>

<script>
import news from "../assets/articles.json";

console.log(news);

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
.link {
    color: black;
    outline: none;
    text-decoration: underline;
    margin: 10px 0;
    font-size: 30px;
}
.article-img {
  margin: 10px 0;
}
</style>