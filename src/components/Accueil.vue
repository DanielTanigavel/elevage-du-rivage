<template>
  <v-parallax
      dark
      src="@/assets/cinqChevaux.jpeg"
      height="1000"
      class="ma-2"
  >
    <v-row
        align="center"
        justify="center"
    >
      <v-col
          class="text-center"
          cols="12"
      >
        <h1 class="text-h4 font-weight-black white--text mb-4 text-uppercase">
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
  </v-parallax>

</template>

<script>
export default {
  name: "Titre"
}
</script>

<style scoped>

</style>