<template>
  <v-card class="mx-auto" max-width="344">
    <v-img v-if="image" :src="require(`@/assets/comidas/${image}`)"></v-img>
    <v-card-title>
      {{ title }}
    </v-card-title>

    <v-card-actions>
      <v-btn color="orange lighten-2" text> Descripción </v-btn>

      <v-spacer></v-spacer>

      <v-btn icon @click="show = !show">
        <v-icon>{{ show ? "mdi-chevron-up" : "mdi-chevron-down" }}</v-icon>
      </v-btn>
    </v-card-actions>

    <v-expand-transition>
      <div v-show="show">
        <v-divider></v-divider>

        <v-card-text>
          {{ description }}
        </v-card-text>
      </div>
    </v-expand-transition>
  </v-card>
</template>

<script lang="ts">
import { defineComponent, ref } from "vue";

export default defineComponent({
  props: {
    title: {
      type: String,
    },
    description: {
      type: String,
    },
    image: {
      type: String,
    },
    price: {
      type: String,
    },
  },
  setup() {
    const show = ref(false);

    return {
      show,
    };
  },
});
</script>
