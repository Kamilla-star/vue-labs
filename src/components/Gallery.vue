<template>
    <v-container>
    <h1 class="intro text-h1 text-center white--text">Галерея</h1>
      <v-row>
        <v-col v-for="(article, i) in news" :key="i" class="d-flex child-flex" cols="6" sm="4">
          <v-card flat tile class="d-flex">
            <v-img :src="require('./../assets/images/'+ article.full_image)" aspect-ratio="1" class="grey lighten-2">
              <template v-slot:placeholder>
                <v-row class="fill-height ma-0" align="center" justify="center">
                  <v-progress-circular indeterminate color="grey lighten-5"></v-progress-circular>
                </v-row>
              </template>
            </v-img>
          </v-card>
        </v-col>
      </v-row>
    </v-container>
</template>

<script>

import news from '../assets/articles.json';

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
.intro {
  margin: 20px 0;
}
</style>