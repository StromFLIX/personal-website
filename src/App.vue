<template>
  <v-app>
    <v-navigation-drawer color="primary" miniVariant="false" fixed dark>
      <v-list dense nav class="py-0">
        <v-list-item two-line :class="miniVariant && 'px-0'">
          <v-list-item-avatar>
            <img
              src="https://avatars3.githubusercontent.com/u/9351775?s=460&u=c79f37e27e4d8ece9b60acd8bdb48386d28f7513&v=4"
            />
          </v-list-item-avatar>

          <v-list-item-content>
            <v-list-item-title>Felix Mönckemeyer</v-list-item-title>
            <v-list-item-subtitle>Fullstack Developer</v-list-item-subtitle>
          </v-list-item-content>
        </v-list-item>

        <v-divider></v-divider>

        <v-list-item v-for="item in items" :key="item.title" link>
          <v-list-item-icon>
            <v-icon>{{ item.icon }}</v-icon>
          </v-list-item-icon>

          <v-list-item-content>
            <v-list-item-title>{{ item.title }}</v-list-item-title>
          </v-list-item-content>
        </v-list-item>
      </v-list>
    </v-navigation-drawer>
    
    <v-content>
      <Profile />
    </v-content>
    
    
    <v-divider inset></v-divider>
    <v-subheader inset>Timeline</v-subheader>
    <v-content>
      <Timeline />
    </v-content>
    <v-divider inset></v-divider>
    <v-subheader inset>Skills</v-subheader>
    <v-content>
      <Skills />
    </v-content>
    
    <v-content>
      <Contact />
    </v-content>
  </v-app>
</template>

<script>
import Timeline from "./components/Timeline";
import Profile from "./components/Profile";
import Contact from "./components/Contact";
import Skills from "./components/Skills";

export default {
  name: "App",

  components: {
    Timeline,
    Profile,
    Contact,
    Skills
  },

  data() {
    return {
      items: [
        { title: "Profile", icon: "mdi-account-circle" },
        { title: "Timeline", icon: "mdi-timeline-outline" },
        { title: "Skills", icon: "mdi-tools" },
        { title: "Contact", icon: "mdi-card-account-mail" }
      ],
      color: "primary",
      colors: ["primary", "blue", "success", "red", "teal"],
      permanent: true,
      miniVariant: true
    };
  }
};
</script>


<style>
.card-text-img {
  display: flex;
  padding: 10px;
}

.title-box {
  display: flex;
}

.title-text-box {
  display: flex;
  flex-direction: column;
  margin-right: auto;
}
.skills {
  display: flex;
  flex-direction: row;
  margin-left: 70px;
  flex-wrap: wrap;
}

.footer {
  width: 100%;
}
</style>