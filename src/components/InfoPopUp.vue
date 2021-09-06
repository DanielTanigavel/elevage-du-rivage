<template>
  <v-row justify="center">
    <v-dialog
        v-model="dialog"
        width="600px"
    >
      <template v-slot:activator="{ on, attrs }">
        <v-hover v-slot="{ hover }">
        <v-btn
            v-bind="attrs"
            v-on="on"
            class="btnPopUp"
            :class="{'show-btns': hover}"
            :color="transparent"
        >
          En savoir plus
        </v-btn>
        </v-hover>
      </template>
      <v-card>
        <v-card-title>
          <span class="text-h5">{{ popUp.subtext }}</span>
        </v-card-title>

        <PopUpCarousel v-bind:imgs="popUp.imgs"/>

        <v-card-text class="mt-4">
          {{ popUp.description }}
        </v-card-text>
        <v-card-actions>
          <v-spacer></v-spacer>
          <v-btn
              color="green darken-1"
              text
              @click="dialog = false"
          >
            Fermer
          </v-btn>
        </v-card-actions>
      </v-card>
    </v-dialog>
  </v-row>
</template>

<script>
import PopUpCarousel from "./PopUpCarousel";

export default {
  components: {PopUpCarousel},
  data() {
    return {
      dialog: false,
      transparent: 'rgba(255, 255, 255, 0)',
    }
  },
  name: "InfoPopUp",
  props: {
    popUp:Array,
  }
}
</script>

<style scoped>
.show-btns {
  color: rgba(255, 255, 255, 1) !important;
}

.btnPopUp {
  opacity: 1;
}
</style>