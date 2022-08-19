<template>
  <Carousel/>
</template>

<script lang="ts">
import { defineComponent } from 'vue';
import Carousel from '@/components/Carousel.vue';

// Components


export default defineComponent({
  name: 'HomeView',

  components: {
    Carousel
},
});
</script>
