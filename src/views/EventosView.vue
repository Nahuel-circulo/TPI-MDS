<template>
  <main class="eventosView">
    <div class="eventosView__header">
      <h1 class="eventosView__header-title">
        EVENTOS CORPORATIVOS Y SALONES PRIVADOS
      </h1>
      <p class="eventosView__header-content">
        Espacios y salones exclusivos ideales para realizar eventos
        corporativos, comidas privadas mientras se disfruta de la mejor comida
        de Argentina. Organizamos comidas exclusivas para grupos, eventos
        corporativos y sociales con capacidad hasta 120. Diseñamos menús para
        cada ocasión con los mejores aperitivos, deliciosas guarniciones y
        riquísimos postres artesanales.
      </p>
    </div>

    <div class="eventosView__gallery">
      <h4 class="eventosView__gallery-title">
        ALGUNAS FOTOGRAFÍAS DE NUESTROS EVENTOS
      </h4>

      <v-row>
        <v-col cols="12" sm="6" md="4" lg="3" v-for="item in 8" :key="item">
          <div class="eventosView__gallery-card">
            <v-img
              class="eventosView__gallery-card__image pointer"
              cover
              @click="viewImageOverlay"
              src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcS-rRUBt97a_Uj-RjiDGlyyGDSQ1qHI9DY32g&usqp=CAU"
            >
            </v-img>
          </div>
        </v-col>
      </v-row>
    </div>

    <v-dialog v-model="overlay" class="image__overlay">
      <v-img
        class="image__overlay-img"
        src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcS-rRUBt97a_Uj-RjiDGlyyGDSQ1qHI9DY32g&usqp=CAU"
      ></v-img>
      <div class="image__overlay-btn mt-4">
        <v-btn color="#BB8A00" :block="false" @click="overlay = false"
          >Cerrar Imagen</v-btn
        >
      </div>
    </v-dialog>
  </main>
</template>

<script lang="ts">
import { defineComponent, ref } from "vue";

export default defineComponent({
  setup() {
    const overlay = ref(false);
    const viewImageOverlay = () => {
      console.log("muestra");
      overlay.value = !overlay.value;
    };

    return {
      overlay,
      viewImageOverlay,
    };
  },
});
</script>

<style lang="scss" scoped>
.pointer {
  cursor: pointer;
}
</style>
