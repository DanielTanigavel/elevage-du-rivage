<template>
  <!--  <v-parallax
        dark
        height="1000"
        src="@/assets/colocChevaux-1.jpg"
    >
      <v-row
          align="center"
          justify="center"
      >
        <v-col
            class="text-center"
            cols="12"
        >
          <h1 class="text-h4 font-weight-black white&#45;&#45;text mb-4 text-uppercase">
            Élevage du rivage
          </h1>
          <h4 class="subheading mb-16">
            Faite nous confiance !
          </h4>
          <v-icon
              color="white"
              large
              class="mt-16"
          >
            mdi-chevron-down
          </v-icon>
        </v-col>
      </v-row>
    </v-parallax>-->
 <!-- <v-carousel
      cycle
      interval="4000"
      height="1000"
      hide-delimiter-background
      show-arrows-on-hover

  >
    <v-carousel-item
        v-for="(img,i) in imgAccueil"
        :key="i"
        :src="imageURL(img)"
    >
      <v-row
          justify="space-center"
          align="center"
          style="height: 100%"
      >
        <v-col
            class="text-center d-flex flex-column justify-center align-center"
            cols="12"
        >
          <p class="text-h4 font-weight-black white--text mb-4 text-uppercase">
            Élevage du rivage
          </p>
          <p class="white--text font-weight-medium mb-16">
            Faite nous confiance !
          </p>
          <v-icon
              color="white"
              large
              class="mt-16"
          >
            mdi-chevron-down
          </v-icon>
        </v-col>
      </v-row>
    </v-carousel-item>
  </v-carousel>-->

<v-content>
  <v-col
      style="height: 100%"
  >
    <v-row
        class="d-flex justify-center align-center ma-10"
    >
      <v-col>
        <p class="text-h1 font-weight-black mb-4 text-uppercase text-center">
          Élevage du rivage
        </p>
        <p class="text-center text-h4 font-weight-medium">
          Élevage de poney et pansion équestre
        </p>
      </v-col>

      <v-card
          elevation="24"
          max-width="850"
          class="mx-auto"
      >
        <v-carousel
            cycle
            interval="3000"
            hide-delimiter-background
            show-arrows-on-hover

        >
          <v-carousel-item
              v-for="(img,i) in imgAccueil"
              :key="i"
              :src="imageURL(img)"
          >
          </v-carousel-item>
        </v-carousel>
      </v-card>
    </v-row>
    <div
        class="d-flex justify-center align-center"
    >
      <v-icon
          color="black"
          large
      >
        mdi-chevron-down
      </v-icon>
    </div>
  </v-col>
</v-content>
</template>

<script>
export default {
  name: "Titre",
  data() {
    return {
      imgAccueil: [
        'colocChevaux.jpg',
        'Sophiane.jpg',
        'mainCheval.jpg'
      ],
    }
  },
  methods: {
    imageURL(p) {
      return require("@/assets/" + p)
    },
  }
}
</script>

<style scoped>

</style>