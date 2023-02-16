<template>
  <v-app dark>
    <v-layout>
      <v-navigation-drawer
        :mini-variant="true"
        color="#e8f7df"
        permanent
      >
        <v-list-item class="px-2">
          <v-list-item-avatar>
            <v-img src="/images/niamhvtag.jpg"></v-img>
          </v-list-item-avatar>

          <v-list-item-title>John Leider</v-list-item-title>
        </v-list-item>

        <v-divider></v-divider>

        <v-list dense>
          <v-list-item
            v-for="item in items"
            :key="item.title"
            link
            :to="item.route"
          >
            <v-list-item-icon>
              <v-icon>{{ item.icon }}</v-icon>
            </v-list-item-icon>

            <v-list-item-content>
              <v-list-item-title>{{ item.title }}</v-list-item-title>
            </v-list-item-content>
          </v-list-item>
        </v-list>
      </v-navigation-drawer>
      <v-main>
        <!-- <v-container> -->
          <Nuxt />
        <!-- </v-container> -->
      </v-main>
    </v-layout>
  </v-app>
</template>

<script>
export default {
  name: 'DefaultLayout',
  data() {
    return {
      items: [
        { title: 'Home', icon: 'mdi-home', route: '/' },
        { title: 'Heart', icon: 'mdi-heart', route: '/heart' },
      ]
    }
  },
}
</script>

<style scoped>
.v-application {
  background-color: #f9fef6;
}
</style>
