<template>
  <v-container>
    <v-card
      class="mx-auto"
      outlined
    >
      <v-list-item three-line>
        <v-list-item-content>
          <v-list-item-title class="headline mb-1">Felix Mönckemeyer</v-list-item-title>
          <v-list-item-subtitle>Fullstack Developer</v-list-item-subtitle>
          <v-img position='left top' class="qrcode" src="/assets/qrcode.png" max-height="150" contain></v-img>
        </v-list-item-content>
  
        <v-list-item-avatar
          tile
          size="200"
        ><img
          src="https://avatars3.githubusercontent.com/u/9351775?s=460&u=c79f37e27e4d8ece9b60acd8bdb48386d28f7513&v=4"
          alt="Felix"
        ></v-list-item-avatar>
      </v-list-item>
    </v-card>
  </v-container>
</template>

<script>
  export default {
    name: 'Profile',

    data: () => ({}),
  }
</script>
