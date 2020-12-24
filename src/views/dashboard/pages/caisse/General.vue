<template>
  <div>
    <v-card-text>
      <template>
        <v-row align="center">
          <v-col cols="5">
            <div class="font-weight-light">
              Montant en pret: {{ caisse.out }} FDj
            </div>
            <div class="font-weight-light">
              Montant disponible: {{ caisse.in }} FDj
            </div>
            <div class="font-weight-light">
              Montant total: {{ caisse.total }} FDj
            </div>
          </v-col>
        </v-row>
      </template>
    </v-card-text>
  </div>
</template>

<script>
  export default {
    data () {
      return {
        caisse: {
          total: '10000000',
          in: '78698709',
          out: '4535647',
        },
      }
    },
  }
</script>
