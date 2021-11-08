<template>
  <div class="d-flex flex-column justify-center align-center ma-5">
    <h2 class="mb-3 font-weight-black">N'hesiter pas à nous contacter </h2>
    <div class="d-flex flex-row justify-center align-center">
      <strong id="mail" class="subheading">{{mail}}</strong>
      <v-btn
        class="mx-2"
        fab
        dark
        small
        color="primary"
        v-on:click="copyTxt"
        >
        <v-icon dark>
          mdi-content-copy
        </v-icon>
      </v-btn>
    </div>


    <h2 class="mb-3 font-weight-black">Ou à venir nous voir ici ! </h2>

    <iframe
        src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d2760.4751774336364!2d-0.853760584194401!3d46.22089439065318!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x4806ccbb8c779271%3A0xf5d728e45de9c3ca!2s29%20Rue%20du%20Gu%C3%A9%2C%2017170%20Saint-Sauveur-d&#39;Aunis!5e0!3m2!1sfr!2sfr!4v1630353197313!5m2!1sfr!2sfr"
        width="600" height="300" style="border:0;" allowfullscreen="" loading="lazy"></iframe>
  </div>

</template>

<script>
export default {
  name: "Maps",
  data: () => ({
    mail: 'elevagedurivage@gmail.com'
  }),
  methods: {
    copyTxt(){
      var copyText = document.querySelector("#mail");
      copyText.select();
      document.execCommand("copy");
    }
  }
}
</script>

<style scoped>

</style>