<template>
  <v-footer inset padless>
    <v-card flat tile inset class="indigo lighten-1 white--text text-center footer">
      <v-card-text>
        <v-btn v-for="social in socials" :key="social" class="mx-4 white--text" icon :href="social.link">
          <v-icon size="24px">{{ social.icon }}</v-icon>
        </v-btn>
      </v-card-text>

      <v-card-text class="white--text">
        {{ new Date().getFullYear() }} —
        <strong>Felix Mönckemeyer</strong>
      </v-card-text>
    </v-card>
  </v-footer>
</template>

<script>
export default {
  name: "Contact",

  data: () => ({
    socials: [
      {
        icon: "fab fa-linkedin",
        link: "https://www.linkedin.com/in/felix-m%C3%B6nckemeyer-6887a61a0/"
      },
      {
        icon: "fab fa-github-square",
        link: "https://github.com/NemesisFLX"
      },
      {
        icon: "fas fa-envelope-square",
        link: "mailto:f.moenckemeyer@gmail.com"
      },
      {
        icon: "fab fa-telegram",
        link: "https://t.me/stromflix"
      }
    ]
  })
};
</script>
