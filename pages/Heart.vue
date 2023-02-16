<template>
  <v-container>
    <v-row>
      <v-col v-for="item in items" :key="item.id" cols="4">
        <v-card color="#fbfcfa" height="400px">
          <v-card-title style="font-weight: bold;">{{ item.title }}</v-card-title>
          <v-card-text style="font-weight: bold;">{{ item.text }}</v-card-text>
        </v-card>
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
export default {
  name: 'IndexPage',
  data() {
    return {
      items: [
        { id: 1, title: 'Lorem ipsum dolor sit amet', text: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Maecenas sem lacus, finibus non eros at, dignissim pretium nunc. Morbi a semper nunc. Nam hendrerit maximus quam, in fermentum eros. Aenean eget magna eget tortor hendrerit pretium. Maecenas a posuere ex, sit amet lacinia elit. Vestibulum vel urna feugiat, cursus ipsum ac, cursus purus. Phasellus eleifend sem non neque volutpat, ut viverra dolor dapibus. Fusce non ligula dapibus, malesuada purus in, vestibulum massa. Aliquam rutrum sollicitudin quam, sit amet egestas erat malesuada non. Duis in fringilla augue. Nunc ullamcorper, velit ac aliquet cursus, magna diam viverra nulla, sed molestie mauris neque a est.' },
        { id: 2, title: 'Donec auctor tellus in rhoncus tincidunt', text: 'Donec auctor tellus in rhoncus tincidunt. Nullam finibus urna magna, sit amet ornare purus tincidunt eu. Donec a mi ac tortor rutrum ultrices a eleifend nunc. Aenean luctus metus eu ante lacinia condimentum. Morbi sem magna, varius vitae placerat vel, posuere eget risus. Vivamus tristique tristique massa, non luctus ante consectetur eu. Vivamus suscipit sem molestie nibh aliquam, in porta nisi molestie.' },
        { id: 3, title: 'Aenean at auctor metus', text: 'Aenean at auctor metus. In eget tempor sem. Quisque quis sagittis massa, non venenatis magna. Vivamus id nisi eget orci faucibus semper ac ac lectus. Donec vulputate, purus eget rhoncus faucibus, magna erat finibus quam, vitae placerat nulla metus at purus. Nulla elementum ex id varius eleifend. Vestibulum lectus ante, placerat a lobortis a, laoreet ac tellus. Donec ante orci, mattis eget faucibus sit amet, luctus ac enim. Vestibulum sagittis tincidunt nibh a volutpat. Aliquam tristique bibendum purus, vel viverra velit viverra ac. Proin nibh magna, egestas ut elementum ut, euismod nec ex. Nunc lobortis leo at dui suscipit, sit amet malesuada nibh suscipit.' },
        { id: 5, title: 'Donec auctor tellus in rhoncus tincidunt', text: 'Donec auctor tellus in rhoncus tincidunt. Nullam finibus urna magna, sit amet ornare purus tincidunt eu. Donec a mi ac tortor rutrum ultrices a eleifend nunc. Aenean luctus metus eu ante lacinia condimentum. Morbi sem magna, varius vitae placerat vel, posuere eget risus. Vivamus tristique tristique massa, non luctus ante consectetur eu. Vivamus suscipit sem molestie nibh aliquam, in porta nisi molestie.' },
        { id: 6, title: 'Aenean at auctor metus', text: 'Aenean at auctor metus. In eget tempor sem. Quisque quis sagittis massa, non venenatis magna. Vivamus id nisi eget orci faucibus semper ac ac lectus. Donec vulputate, purus eget rhoncus faucibus, magna erat finibus quam, vitae placerat nulla metus at purus. Nulla elementum ex id varius eleifend. Vestibulum lectus ante, placerat a lobortis a, laoreet ac tellus. Donec ante orci, mattis eget faucibus sit amet, luctus ac enim. Vestibulum sagittis tincidunt nibh a volutpat. Aliquam tristique bibendum purus, vel viverra velit viverra ac. Proin nibh magna, egestas ut elementum ut, euismod nec ex. Nunc lobortis leo at dui suscipit, sit amet malesuada nibh suscipit.' },
        { id: 4, title: 'Lorem ipsum dolor sit amet', text: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Maecenas sem lacus, finibus non eros at, dignissim pretium nunc. Morbi a semper nunc. Nam hendrerit maximus quam, in fermentum eros. Aenean eget magna eget tortor hendrerit pretium. Maecenas a posuere ex, sit amet lacinia elit. Vestibulum vel urna feugiat, cursus ipsum ac, cursus purus. Phasellus eleifend sem non neque volutpat, ut viverra dolor dapibus. Fusce non ligula dapibus, malesuada purus in, vestibulum massa. Aliquam rutrum sollicitudin quam, sit amet egestas erat malesuada non. Duis in fringilla augue. Nunc ullamcorper, velit ac aliquet cursus, magna diam viverra nulla, sed molestie mauris neque a est.' },
        { id: 9, title: 'Aenean at auctor metus', text: 'Aenean at auctor metus. In eget tempor sem. Quisque quis sagittis massa, non venenatis magna. Vivamus id nisi eget orci faucibus semper ac ac lectus. Donec vulputate, purus eget rhoncus faucibus, magna erat finibus quam, vitae placerat nulla metus at purus. Nulla elementum ex id varius eleifend. Vestibulum lectus ante, placerat a lobortis a, laoreet ac tellus. Donec ante orci, mattis eget faucibus sit amet, luctus ac enim. Vestibulum sagittis tincidunt nibh a volutpat. Aliquam tristique bibendum purus, vel viverra velit viverra ac. Proin nibh magna, egestas ut elementum ut, euismod nec ex. Nunc lobortis leo at dui suscipit, sit amet malesuada nibh suscipit.' },
        { id: 7, title: 'Lorem ipsum dolor sit amet', text: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Maecenas sem lacus, finibus non eros at, dignissim pretium nunc. Morbi a semper nunc. Nam hendrerit maximus quam, in fermentum eros. Aenean eget magna eget tortor hendrerit pretium. Maecenas a posuere ex, sit amet lacinia elit. Vestibulum vel urna feugiat, cursus ipsum ac, cursus purus. Phasellus eleifend sem non neque volutpat, ut viverra dolor dapibus. Fusce non ligula dapibus, malesuada purus in, vestibulum massa. Aliquam rutrum sollicitudin quam, sit amet egestas erat malesuada non. Duis in fringilla augue. Nunc ullamcorper, velit ac aliquet cursus, magna diam viverra nulla, sed molestie mauris neque a est.' },
        { id: 8, title: 'Donec auctor tellus in rhoncus tincidunt', text: 'Donec auctor tellus in rhoncus tincidunt. Nullam finibus urna magna, sit amet ornare purus tincidunt eu. Donec a mi ac tortor rutrum ultrices a eleifend nunc. Aenean luctus metus eu ante lacinia condimentum. Morbi sem magna, varius vitae placerat vel, posuere eget risus. Vivamus tristique tristique massa, non luctus ante consectetur eu. Vivamus suscipit sem molestie nibh aliquam, in porta nisi molestie.' },
      ]
    }
  },
}
</script>
