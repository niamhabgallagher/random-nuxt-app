<template>
  <v-app dark>
    <v-app-bar fixed app>
      <v-toolbar-title>Random Nuxt App</v-toolbar-title>
    </v-app-bar>
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
      <v-item v-for="item in items" :key="item.num" style="margin: 15px">
        <v-card>
          <v-card-title>{{ item.title }}</v-card-title>
          <v-card-text>
            <v-progress-linear indeterminate :color="item.color"></v-progress-linear>
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
        { title: 'Loading 1', num: 1, color: 'primary' },
        { title: 'Loading 2', num: 2, color: 'secondary' },
        { title: 'Loading 3', num: 3, color: 'warning' },
        { title: 'Loading 4', num: 4, color: 'success' },
      ],
      fab: false
    }
  },
}
</script>
