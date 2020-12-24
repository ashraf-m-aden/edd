<template>
  <div>
    <base-material-card
      icon="mdi-account"
      title="Ismael Ali Abdi"
      class="px-5 py-3"
    >
      <v-list
        nav
        dense
      >
        <v-list-item-group
          v-model="selectedItem"
          color="primary"
        >
          <v-list-item
            v-for="(item, i) in items"
            :key="i"
          >
            <v-list-item-icon>
              <v-icon v-text="item.icon" />
            </v-list-item-icon>

            <v-list-item-content>
              <v-list-item-title v-text="item.text" />
            </v-list-item-content>
          </v-list-item>
        </v-list-item-group>
      </v-list>
    </base-material-card>
    <base-material-card
      icon="mdi-cash"
      title="Historique de crédit"
      class="px-5 py-3"
    >
      <v-simple-table>
        <thead>
          <tr>
            <th class="primary--text">
              Date debut
            </th>
            <th class="primary--text">
              Montant
            </th>
            <th class="primary--text">
              Echéance
            </th>
            <th class="primary--text">
              Status
            </th>
          </tr>
        </thead>

        <tbody>
          <tr>
            <td>Jan 2019</td>
            <td>1352462 FDj</td>
            <td>2</td>
            <td>Remboursé</td>
          </tr>
          <tr>
            <td>Jan 2019</td>
            <td>1352462 FDj</td>
            <td>2</td>
            <td>Remboursé</td>
          </tr>
          <tr>
            <td>Jan 2019</td>
            <td>1352462 FDj</td>
            <td>2</td>
            <td>Remboursé</td>
          </tr>
          <tr>
            <td>Jan 2019</td>
            <td>1352462 FDj</td>
            <td>2</td>
            <td>Remboursé</td>
          </tr>
        </tbody>
      </v-simple-table>
    </base-material-card>
  </div>
</template>
<script>
  export default {
    data: () => ({
      selectedItem: 0,
      items: [
        { text: 'Departement', icon: 'mdi-folder' },
        { text: 'Position', icon: 'mdi-account-settings' },
        { text: 'Numero', icon: 'mdi-phone' },
        { text: 'Email', icon: 'mdi-at' },
        { text: 'Addresse', icon: 'mdi-navigation' },
      ],
    }),
  }
</script>
