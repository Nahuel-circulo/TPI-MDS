<template>
  <div>
    <h1>Reservas</h1>
    <v-row class="pa-0 ma-0">
      <v-col class="d-flex justify-center" cols="3" v-for="(item, i) in tables" :key="i">
        <v-icon
          @click="changeColor(item.position)"
          :color="item.reservado ? 'blue' : 'black'"
          >mdi-table-chair</v-icon
        >
      </v-col>
    </v-row>
  </div>
</template>

<script lang="ts">
import { defineComponent, ref } from "vue";

export default defineComponent({
  setup() {
    const tables = ref([
      {
        position: 1,
        reservado: false,
      },
      {
        position: 2,
        reservado: false,
      },
      {
        position: 3,
        reservado: true,
      },
      {
        position: 4,
        reservado: false,
      },
      {
        position: 5,
        reservado: false,
      },
      {
        position: 6,
        reservado: false,
      },
      {
        position: 7,
        reservado: false,
      },
      {
        position: 8,
        reservado: false,
      },
      {
        position: 9,
        reservado: false,
      },
      {
        position: 10,
        reservado: false,
      },
      {
        position: 11,
        reservado: false,
      },
      {
        position: 12,
        reservado: false,
      },
      {
        position: 13,
        reservado: false,
      },
      {
        position: 14,
        reservado: false,
      },
      {
        position: 15,
        reservado: false,
      },
      {
        position: 16,
        reservado: false,
      },
      {
        position: 17,
        reservado: false,
      },
      {
        position: 18,
        reservado: false,
      },
      {
        position: 19,
        reservado: false,
      },
      {
        position: 20,
        reservado: false,
      },
    ]);
    const changeColor = (position: number) => {
      const index = tables.value.findIndex(
        (table) => table.position === position
      );
      tables.value[index].reservado = !tables.value[index].reservado;
    };
    return {
      changeColor,
      tables,
    };
  },
});
</script>
