<template>
  <v-carousel cycle height="400" hide-delimiter-background hide-delimiters show-arrows-on-hover>
    <v-carousel-item v-for="(slide, i) in images" :key="i" >
      <v-img :src="slide" cover ></v-img>
    </v-carousel-item>
  </v-carousel>
</template>

<script lang="ts">
import { defineComponent } from "vue";

export default defineComponent({
  setup() {
    const images = [
      "https://www.restaurantenodo.es/wp-content/uploads/2019/06/restaurant-food-salat-2.jpg",
      "https://i0.wp.com/cravedfw.com/wp-content/uploads/2020/07/071620_ngon_kathytran_054a5174.jpg",

    ];
    

    return {
      images
    };
  },
});
</script>
