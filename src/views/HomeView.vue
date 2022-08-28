<template>
  <main class="homeView">
    <Carousel />
    <div class="reserva-section">
      <v-btn plain elevation="0" block class="reserva-section__btn">
        Reserva aquí
      </v-btn>
    </div>
  </main>
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
