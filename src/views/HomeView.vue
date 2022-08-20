<template>
  <div>
    <Carousel />
  </div>
</template>

<script lang="ts">
import { defineComponent } from "vue";
import Carousel from "@/components/Carousel.vue";

export default defineComponent({
  name: "HomeView",

  components: {
    Carousel,
  },
  setup() {
    return {};
  },
});
</script>
