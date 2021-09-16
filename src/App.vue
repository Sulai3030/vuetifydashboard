<template>
  <v-app>
    <v-app-bar app color="primary" dark>
      <v-app-toolbar-title> Vuetify Dashboard </v-app-toolbar-title>
      <v-spacer></v-spacer>
      <v-btn
        v-for="link in links"
        y
        :key="`${link.label}-header-link`"
        text
        rounded
        :to="link.url"
      >
        {{ link.label }}
      </v-btn>
    </v-app-bar>
    <v-content></v-content>
    <v-spacer></v-spacer>
    <router-view></router-view>
    <v-footer color="primary lighten-1" padless>
      <v-row justify="center" no-gutters>
        <v-btn
          v-for="link in links"
          y
          :key="`${link.label}-header-link`"
          text
          rounded
          :to="link.url"
        >
          {{ link.label }}
        </v-btn>
        <v-flex primary lighten-2 py-4 text-center white--text xs-12> </v-flex>
        <v-col class="primary lighten-2 py-4 text-center white--text" cols="12">
          {{ new Date().getFullYear() }} — <strong>Vuetify</strong>
        </v-col>
      </v-row>
    </v-footer>
  </v-app>
</template>

<script>
export default {
  name: "App",
  data() {
    return {
      showPassword: false,
      links: [
        {
          label: "Home",
          url: "/",
        },
        {
          label: "login",
          url: "login",
        },
        {
          label: "About",
          url: "about",
        },
        {
          label: "Dashboard",
          url: "dashboard",
        },
      ],
    };
  },
};
</script>
