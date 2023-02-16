<template>
  <v-container>
    <div v-for="items in accounts" :key="items.id">
      <v-row style="margin: 10px">
        <v-col v-for="item in items.people" :key="item.id" cols="4">
          <v-card color="#f9fef6" elevation="0">
            <v-card-title style="font-weight: bold;">{{ item.name }}</v-card-title>
            <v-card-subtitle style="font-weight: bold;">{{ item.description }}</v-card-subtitle>
            <v-chip
              class="ma-2"
              color="primary"
              style="font-weight: bold;"
            >
              {{ item.skills[0] }}
            </v-chip>
            <v-chip
              class="ma-2"
              color="secondary"
              style="font-weight: bold;"
            >
              {{ item.skills[1] }}
            </v-chip>
            <v-chip
              class="ma-2"
              color="tertiary"
              style="font-weight: bold;"
            >
              {{ item.skills[2] }}
            </v-chip>
          </v-card>
        </v-col>
      </v-row>
      <v-divider></v-divider>
    </div>
  </v-container>
</template>

<script>
export default {
  name: 'IndexPage',
  data() {
    return {
      accounts: [
        {
          id: 1,
          people: [
            { id: 1, name: 'Niamh', description: 'Is a programmer', skills: [ 'Web', 'Smoothie Bowls', 'Coffee' ] },
            { id: 2, name: 'Soup', description: 'Is a whippet', skills: [ 'Running fast', 'Eating', 'Being Cute' ] },
            { id: 3, name: 'Bronagh', description: 'Is a school student', skills: [ 'Irish Dancing', 'Maths', 'Sport' ] }
          ]
        },
        {
          id: 2,
          people: [
            { id: 3, name: 'Bronagh', description: 'Is a school student', skills: [ 'Irish Dancing', 'Maths', 'Sport' ] },
            { id: 1, name: 'Niamh', description: 'Is a programmer', skills: [ 'Web', 'Smoothie Bowls', 'Coffee' ] },
            { id: 2, name: 'Soup', description: 'Is a whippet', skills: [ 'Running fast', 'Eating', 'Being Cute' ] },
          ]
        },
        {
          id: 3,
          people: [
            { id: 2, name: 'Soup', description: 'Is a whippet', skills: [ 'Running fast', 'Eating', 'Being Cute' ] },
            { id: 3, name: 'Bronagh', description: 'Is a school student', skills: [ 'Irish Dancing', 'Maths', 'Sport' ] },
            { id: 1, name: 'Niamh', description: 'Is a programmer', skills: [ 'Web', 'Smoothie Bowls', 'Coffee' ] },
          ]
        },
      ]
    }
  },
}
</script>