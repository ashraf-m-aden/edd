<template>
  <v-container
    id="regular-tables"
    fluid
    tag="section"
  >
    <v-row>
      <v-col
        cols="6"
        class="d-flex justify-center"
      >
        <v-text-field
          label="Recherche"
          color="secondary"
          hide-details
          style="minx-width: 165px;"
        >
          <template
            v-if="$vuetify.breakpoint.mdAndUp"
            v-slot:append-outer
          >
            <v-btn
              class="mt-n2"
              elevation="1"
              fab
              small
            >
              <v-icon>mdi-magnify</v-icon>
            </v-btn>
          </template>
        </v-text-field>
      </v-col>
      <v-col
        class="d-flex justify-end"
        cols="6"
      >
        <v-btn
          small
          color="success"
          class="mr-0"
          @click="createNewEmploye"
        >
          Creer nouveau profil
        </v-btn>
      </v-col>
    </v-row>
    <base-material-card
      icon="mdi-clipboard-text"
      title="La liste de tous les employés"
      class="px-5 py-3"
    >
      <v-simple-table>
        <thead>
          <tr>
            <th class="primary--text">
              Name
            </th>
            <th class="primary--text">
              Matricule
            </th>
            <th class="primary--text">
              Position
            </th>
          </tr>
        </thead>

        <tbody>
          <tr @click="goDetails">
            <td>Dakota Rice</td>
            <td>1352462</td>
            <td>Agent</td>
          </tr>

          <tr @click="goDetails">
            <td>Minverva Hooper</td>
            <td>1352462</td>
            <td>Agent</td>
          </tr>

          <tr @click="goDetails">
            <td>Sage Rodriguez</td>
            <td>1352462</td>
            <td>Agent</td>
          </tr>

          <tr @click="goDetails">
            <td>Philip Chaney</td>
            <td>1352462</td>
            <td>Agent</td>
          </tr>

          <tr @click="goDetails">
            <td>Doris Greene</td>
            <td>1352462</td>
            <td>Agent</td>
          </tr>

          <tr @click="goDetails">
            <td>Mason Porter</td>
            <td>1352462</td>
            <td>Agent</td>
          </tr>
        </tbody>
      </v-simple-table>
    </base-material-card>
  </v-container>
</template>

<script>
  export default {
    methods: {
      goDetails () {
        this.$router.push({ path: '/tables/employe-details' })
      },
      createNewEmploye () {
        this.$router.push({ path: '/tables/nouveau-employe' })
      },
    },
  }
</script>
