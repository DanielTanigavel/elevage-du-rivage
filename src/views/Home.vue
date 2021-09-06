<template>
  <v-responsive
      class="overflow-y-auto"
  >
    <Titre/>

    <v-responsive
        class="text-center"
    >

      <v-divider></v-divider>
      <Information v-bind:infos="infos"/>
      <v-divider></v-divider>
      <Maps/>
    </v-responsive>
    <Footer/>
  </v-responsive>
</template>

<script>
import Titre from '../components/Accueil'
import Information from "../components/Information";
import Footer from "../components/Footer";
import Maps from "../components/Maps";

export default {
  name: 'Home',

  data: () => {
    return {
      infos: [
        {
          titre: "Qui sommes-nous ?",
          img: "clemanceEtColoc.jpeg",
                 },
        {
          titre: "uiofgdhiouezhg ? ?",
          img: "clemanceEtColoc.jpeg",
                  },
        {
          titre: "Notre projet",
          img: "clemanceCheval.jpg",

        },
        {
          titre: "qiodcbvqdsbvcoi",
          img: "clemanceCheval.jpg",

        }
      ],
    }
  },

  components: {
    Maps,
    Footer,
    Information,
    // eslint-disable-next-line vue/no-unused-components
    Titre
  },
}
</script>

<style>
html {
  margin: 0;
  padding: 0;
}

body {
  display: flex;
  flex-direction: column;
  min-height: 100%;
}
</style>