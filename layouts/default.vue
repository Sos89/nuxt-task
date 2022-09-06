<template>
  <v-app>
    <v-app-bar>
      <app-bar></app-bar>
    </v-app-bar>
    <v-navigation-drawer permanent light width="280">
      <app-menu></app-menu>
    </v-navigation-drawer>
    <v-main>
      <v-container fluid>
        <router-view></router-view>
      </v-container>
    </v-main>
  </v-app>
</template>

<script>
import AppBar from "~/components/layouts/app-bar";
import AppMenu from "~/components/layouts/app-menu";
export default {
  name: 'DefaultLayout',
  components: {AppMenu, AppBar},
}
</script>
<style>
.theme--dark.v-application{
  background: #ffffff;
  color: black;
}
</style>
