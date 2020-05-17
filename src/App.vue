<template>
  <v-app>
    <v-app-bar
      app
      color="primary"
      dark
    >
      <div class="d-flex align-center">
        <v-img
          alt="Vuetify Logo"
          class="shrink mr-2"
          contain
          src="https://cdn.vuetifyjs.com/images/logos/vuetify-logo-dark.png"
          transition="scale-transition"
          width="40"
        />

        <v-img
          alt="Vuetify Name"
          class="shrink mt-1 hidden-sm-and-down"
          contain
          min-width="100"
          src="https://cdn.vuetifyjs.com/images/logos/vuetify-name-dark.png"
          width="100"
        />
      </div>

      <v-spacer></v-spacer>

      <v-btn
        href="https://github.com/vuetifyjs/vuetify/releases/latest"
        target="_blank"
        text
      >
        <span class="mr-2">Latest Release</span>
        <v-icon>mdi-open-in-new</v-icon>
      </v-btn>
    </v-app-bar>
    <v-content>
      <Profile/>
    </v-content>
    <v-content>
      <Timeline/>
    </v-content>
    <v-content>
      <Skills/>
    </v-content>
    <v-content>
      <Contact/>
    </v-content>
  </v-app>
</template>

<script>
import Timeline from './components/Timeline';
import Profile from './components/Profile';
import Contact from './components/Contact';
import Skills from './components/Skills';

export default {
  name: 'App',

  components: {
    Timeline,
    Profile,
    Contact,
    Skills
  },

  data: () => ({
    //
  }),
};
</script>
