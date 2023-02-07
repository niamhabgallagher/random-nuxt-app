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
    <v-footer style="background-color: #fff;">
      <v-btn color="primary" style="margin: 10px;" fab>
        <v-icon>mdi-format-list-bulleted</v-icon>
      </v-btn>
    </v-footer>
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
        { title: 'Loading 3', num: 3, color: 'tertiary' },
        { title: 'Loading 4', num: 4, color: 'success' },
      ]
    }
  },
}
</script>
