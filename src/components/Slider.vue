<template>
  <v-carousel
    cycle
    height="400"
    hide-delimiter-background
    show-arrows-on-hover
  >
    <v-carousel-item
      v-for="(article, i) in slides"
      :key="i"
    > 
      <v-sheet
        :color="colors[i]"
        height="100%"
        v-if="article.slider"
      >
        <v-row
          class="fill-height"
          align="center"
          justify="center"
        >
          <div class="text-h4">
            {{ article.name }}
          </div>
        </v-row>
      </v-sheet>
    </v-carousel-item>
  </v-carousel>
</template>

<script>
  import news from '../assets/articles.json';
  const slides = news.filter(item => item.slider === true);

  const colors = [
    'pink darken-2',
    'red lighten-1',
    'deep-purple accent-4',
];
  
  export default {
    data () {
      return {
        slides,
        colors,
      }
    },
  }
</script>