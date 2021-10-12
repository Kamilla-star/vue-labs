<template>
    <div class="text-center">
        <span class="text-h1">волк не тот кто walk а тот кто волк</span>
        <Slider/>
        <span class="text-h3">Саттарова Камилла 201-322</span> 
    </div>
</template>

<script>
import Slider from '@/components/Slider.vue'

export default {
  name: "Home",
  components: {
      Slider
  },
};
</script>

<style>
span {
  color: #fff;
}
</style>