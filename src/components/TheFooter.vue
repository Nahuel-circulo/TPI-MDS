<template>
  <v-footer class="footer font-inter">
    <div class="footer__container">
      <router-link class="footer__logo" to="/">
        <img :src="require('../assets/logo.svg')" alt="" />
      </router-link>
      <div class="footer__information">
        <div class="footer__location">
          <h3 class="footer__location-title">Sede Central Resistencia</h3>
          <p class="footer__location-address">
            <v-icon class="footer__location-icon">mdi-map-marker</v-icon>French
            405, Resistencia Chaco.
          </p>
          <p class="footer__location-phone">
            <v-icon class="footer__location-icon">mdi-phone</v-icon>(011)
            5544-7000
          </p>
        </div>
        <div class="footer__social-media">
          <a style="{{'text-decoration': 'none';}}"
            href="https://www.linkedin.com/company/powgen-diesel-s-a/"
            target="_blank"
            ><v-icon class="footer__location-icon">mdi-twitter</v-icon></a>
          <a style="{{'text-decoration': 'none';}}" href="https://www.facebook.com/powgensa" target="_blank"
            ><v-icon class="footer__location-icon">mdi-facebook</v-icon></a>
          <a style="{{'text-decoration': 'none';}}" href="https://www.instagram.com/powgenargentina/" target="_blank"
            ><v-icon class="footer__location-icon">mdi-instagram</v-icon></a>
        </div>
      </div>

      <div class="footer__copyright">
        <p>© 2022 Sentidos® | Todos los derechos reservados.</p>

        <p>
          Creado por DevStation
          <!-- <span> <img src="/icons/footer/CirculoLogo.svg" alt="" /></span> -->
        </p>
      </div>
    </div>
  </v-footer>
</template>
<script lang="ts">
import { defineComponent } from "vue";

export default defineComponent({
  setup() {
    return {};
  },
});
</script>
