<template>
  <div>
    <v-row>
      <v-col cols="12">
        <base-material-card class="px-5 py-3">
          <template v-slot:heading>
            <v-tabs
              v-model="tabs"
              background-color="transparent"
              slider-color="white"
            >
              <v-tab class="mr-3">
                <v-icon class="mr-2">
                  mdi-bug
                </v-icon>
                Informations generales
              </v-tab>

              <v-tab class="mr-3">
                <v-icon class="mr-2">
                  mdi-bug
                </v-icon>
                Statistiques
              </v-tab>

              <v-tab class="mr-3">
                <v-icon class="mr-2">
                  mdi-bug
                </v-icon>
                Fin de pret
              </v-tab>
            </v-tabs>
          </template>

          <v-tabs-items
            v-model="tabs"
            class="transparent"
          >
            <v-tab-item
              v-for="n in 3"
              :key="n"
            >
              <general-information v-show="tabs==0" />
              <caisse-statistiques v-show="tabs==1" />
              <fin-pret v-show="tabs==2" />
            </v-tab-item>
          </v-tabs-items>
        </base-material-card>
      </v-col>
    </v-row>
  </div>
</template>

<script>
  export default {
    components: {
      GeneralInformation: () => import('./General'),
      CaisseStatistiques: () => import('./Statistiques'),
      FinPret: () => import('./FinPret'),
    },
    data () {
      return {
        tabs: 0,
      }
    },
  }
</script>
