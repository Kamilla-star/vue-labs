<template>
  <main class="text-center">
    <h1 class="text-h1">{{news[id-1].name}}</h1>
        <v-img
        aspect-ratio="4"
            :src="require('./../assets/images/' + news[id-1].full_image)"
        ></v-img>
    <div class='text-h3 ma-15'>
        {{news[id-1].desc}}
    </div>
    <div class='text-h4'>
       Дата: {{news[id-1].date}}
    </div>
  </main>
</template>

<script>
import news from '@/assets/articles.json'
export default {
  name: 'Article',
  props: ['id'],
  data(){
      return {
        news: news
    };
  }
}
</script>

<style scoped>

</style>