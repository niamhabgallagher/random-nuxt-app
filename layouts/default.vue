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
      <v-badge color="red" :content="items.length" overlap>
        <v-icon color="primary" style="margin: 10px;" large>mdi-format-list-bulleted</v-icon>
      </v-badge>
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
