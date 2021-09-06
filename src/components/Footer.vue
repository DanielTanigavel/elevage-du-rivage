<template>
  <v-footer
      dark
      padless
  >
    <v-card
        class="flex"
        flat
        tile
    >
      <v-card-title class="py-2 green darken-3">
        <strong class="subheading">Suivez nous sur les réseaux pour ne rien manquer !</strong>

        <v-spacer></v-spacer>

        <v-btn
            v-for="icon in icons"
            :key="icon"
            class="mx-4"
            dark
            icon
            :href="icon.lien"
            target="_blank"
        >
            <v-icon size="24px">
              {{ icon.ic }}
            </v-icon>
        </v-btn>
      </v-card-title>

      <v-card-text class="py-2 text-center">
        {{ new Date().getFullYear() }} — <strong>Tanigavel Daniel</strong>
      </v-card-text>
    </v-card>
  </v-footer>
</template>

<script>
export default {
  name: "Footer",
  data: () => ({
    icons: [
      {
        ic: 'mdi-facebook',
        lien: 'https://facebook.com'
      },
      {
        ic: 'mdi-instagram',
        lien: 'https://instagram.com'
      },
    ],
  }),
}
</script>

<style scoped>
</style>