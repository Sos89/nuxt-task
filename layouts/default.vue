<template>
  <v-app>
    <v-app-bar app style="width: 100%; left: 0; box-shadow: none">
      <app-bar></app-bar>
    </v-app-bar>
    <v-navigation-drawer app permanent width="280" style="margin-top: 64px;">
      <app-menu></app-menu>
    </v-navigation-drawer>
    <v-main style="padding: 0">
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
.v-toolbar__content{
  padding: 0;
  margin: 0;
}
.theme--dark.v-application{
  background: #ffffff;
  color: black;
}
</style>
