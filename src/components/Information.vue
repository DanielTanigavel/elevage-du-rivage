<template>
  <v-container class="pa-4 text-center">
    <v-row
        class="fill-height"
        align="center"
        justify="center"
    >
      <template v-for="(item, i) in items">
        <v-col
            :key="i"
            cols="12"
            md="4"
        >
          <v-hover v-slot="{ hover }">
            <v-card
                :elevation="hover ? 12 : 2"
                :class="{ 'on-hover': hover }"
                class="infoCard"
            >
              <v-img
                  :src=imageURL(item.img)
                  height="300px"
              >
                <v-card-title class="text-h6 white--text">
                  <v-row
                      class="fill-height flex-column"
                      justify="space-between"
                  >
                    <p class="mt-3 subheading font-weight-black">
                      {{ item.title }}
                    </p>

                    <div>
                      <p class="ma-2 text-body-1 font-weight-bold font-italic text-left">
                        {{ item.text }}
                      </p>
                    </div>
                  </v-row>
                </v-card-title>
                <InfoPopUp v-bind:pop-up="item.popUp"/>
              </v-img>
            </v-card>
          </v-hover>
        </v-col>
      </template>
    </v-row>
  </v-container>

</template>

<script>

/*
import Paralaxe from "./Paralaxe";
*/
/*
import Nous from "./Fixe";
*/
import InfoPopUp from "./InfoPopUp";

export default {
  name: "Information",

  components: {InfoPopUp},
  data: () => ({
    items: [
      {
        title: 'Qui sommes-nous ?',
        text: `Nous sommes genial !`,
        img: 'chevalFace.jpg',
        popUp: {
          subtext: 'Nous sommes genial !',
          description: 'Bienvenu à l’élevage du Rivage.\n' +
              '\n' +
              'Nous vous accueillions vous et vos chevaux dans un environnement paisible et reposant.\n' +
              'Différents types de pensions vous seront proposés. Au pré à l’année en troupeau, vos amis à quatre pattes retrouveront leurs libertés. Les chevaux auront accès à un abri et à l’eau dans des prés sécurisés par nos caméras et clôtures électriques.',
          imgs: [
            'chevalOeil.jpg',
            'chevalProfile.jpg',
            'chevalPres.jpg'
          ]
        },
      },
      {
        title: 'Notre Projet',
        text: 'Parce que c\'est notre projet !',
        img: 'chevalFoin.jpg',
        popUp: {
          subtext: 'Parce que c\'est notre projet !',
          description: 'Avec notre alimentation équilibrée et adaptée, vos chevaux seront en pleine forme !  La pension comprend une ration de granulé Haven’s matin et soir, ainsi que du foin d’une qualité exceptionnelle récolté par nos propre soins en plein cœur du marais poitevin.\n' +
              'Vous pourrez profiter de notre carrière privée afin de pouvoir y monter en toute tranquillité. De même la proximité avec la foret de Benon vous offrira de nombreuses possibilités de balades et randonnées en toutes saisons. Après vos longues promenades notre espace dédié aux soins avec douche, boxes et sellerie vous permettra de rester proche de votre compagnon tout en prenant soins de lui.',
          imgs: [
            'chevalTrot.jpg',
            'mainCheval.jpg',
            'coupleCheval.jpg'
          ]
        },
      },
      {
        title: 'Notre élevage',
        text: 'Vive les poneys',
        img: 'familleCheval.jpg',
        popUp: {
          subtext: 'Vive les poneys',
          description: 'Spécialisées dans l’élevage de poney de sport, nous donnons naissance chaque année à des poulains, que nous élevons et valorisons pour la vente. Possédant pour l’instant deux poulinières, nous espérons agrandir notre cheptel en avançant à vos côtés et en vous faisant profiter de notre savoir-faire et de nos expériences dans le domaine.\n' +

              'Vous rêvez d’un havre de paix pour votre cheval, loin des boxes et du stress ?\n' +
              'N’hésitez plus, contactez-nous afin d’échanger de vive voix de notre passion commune !',
          imgs: [
            'familleNB.jpg',
            'poulain.jpg',
            'poulainMere.jpg'
          ]
        },
      },
    ],
    transparent: 'rgba(255, 255, 255, 0)',
  }),
  methods: {
    imageURL(p) {
      return require("@/assets/" + p)
    },
  }
}
</script>

<style scoped>
/*ul {
  list-style: none;
}*/
.infoCard {
  transition: opacity .4s ease-in-out;
}

.infoCard:not(.on-hover) {
  opacity: 0.8;
}

.show-btns {
  color: rgba(255, 255, 255, 1) !important;
}
</style>