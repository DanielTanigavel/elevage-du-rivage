<template>
  <v-carousel
      cycle
      interval="4000"
      height="400"
      hide-delimiter-background
      show-arrows-on-hover
      class="pa-1"
  >
    <v-carousel-item
        v-for="(img,i) in imgs"
        :key="i"
        :src="imageURL(img)"
    >
    </v-carousel-item>
  </v-carousel>
</template>

<script>
export default {
  name: "PopUpCarousel",
  data() {
    return {

    }
  },
  props: {
    imgs: Array,
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