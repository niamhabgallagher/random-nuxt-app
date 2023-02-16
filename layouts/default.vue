<template>
  <v-app dark>
    <v-main>
      <v-container>
        <Nuxt />
      </v-container>
    </v-main>
    <!-- <v-footer style="background-color: #fff;">
      <v-btn class="mx-2" fab dark color="teal" style="margin: 20px">
        <v-badge color="red" :content="items.length" >
          <v-icon dark>
            mdi-format-list-bulleted-square
          </v-icon>
        </v-badge>
      </v-btn>
    </v-footer> -->
    <v-speed-dial 
      v-model="fab"
      bottom left
      direction="top"
      style="width: 15%"
    >
    <template #activator>
      <v-btn v-model="fab" color="blue darken-2" dark fab>
        <v-badge color="red" :content="items.length">
          <v-icon v-if="fab" dark>
            mdi-close
          </v-icon>
          <v-icon v-else dark>
            mdi-format-list-bulleted-square
          </v-icon>
        </v-badge>
      </v-btn>
    </template>
    <v-item-group style="width: 100%">
      <v-item v-for="item in items" :key="item.id" style="margin: 15px">
        <v-card>
          <v-card-title>{{ item.name }} ({{ item.id }})</v-card-title>
          <v-card-text>
            <v-label>{{ item.job }}</v-label>
            <v-progress-linear :value="item.progress" color="primary"></v-progress-linear>
          </v-card-text>
        </v-card>
      </v-item>
    </v-item-group>
  </v-speed-dial>
  </v-app>
</template>

<script>
export default {
  name: 'DefaultLayout',
  data() {
    return {
      items: [
        { id: 0, name: 'Import Session', job: 'Downloading file', progress: 0 },
        { id: 1, name: 'Import Session', job: 'Downloading file', progress: 30 },
        { id: 2, name: 'Import Session', job: 'Downloading file', progress: 10 },
        { id: 3, name: 'Import Session', job: 'Downloading file', progress: 20 },
      ],
      fab: false
    }
  },
}
</script>

<style scoped>
.v-application {
  background-color: #f9fef6;
}
</style>
