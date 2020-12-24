<template>
  <div>
    <v-card-text>
      <template v-for="(task, i) in data">
        <v-row
          :key="i"
          align="center"
        >
          <v-col cols="5">
            <div
              class="font-weight-light"
              v-text="task.text"
            />
          </v-col>
          <v-col cols="5">
            <div
              class="font-weight-light"
              v-text="task.mat"
            />
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
        data: [
          {
            text: 'Ilyas Osman',
            mat: '34567',
          },
          {
            text: 'Amina Igueh',
            mat: '34567',
          },
          {
            text: 'Bilal Nour',
            mat: '34567',
          },
          { text: 'Sougueh Farah', mat: '34567' },
        ],
      }
    },
  }
</script>
