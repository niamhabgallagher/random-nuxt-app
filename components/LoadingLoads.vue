<template>
  <v-speed-dial 
    v-model="fab"
    bottom left
    direction="top"
    style="width: 15%"
  >
    <template #activator>
      <v-btn v-model="fab" color="primary" dark fab>
        <v-badge color="secondary" :content="items.length">
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
</template>

<script>
export default {
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