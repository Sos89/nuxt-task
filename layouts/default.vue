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
  components: {
    AppMenu,
    AppBar,
  },
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
.paragraph{
  font-family: 'Neue Haas Grotesk Text Pro';
  font-style: normal;
  font-weight: 700;
  font-size: 30px;
  line-height: 38px;
  color: #000000;
  margin-top: 154px;
  margin-right: auto;
}
.payer{
  font-family: 'Neue Haas Grotesk Text Pro';
  font-style: normal;
  font-weight: 400;
  font-size: 20px;
  line-height: 24px;
  color: #000000;
}
.rec-details{
  display: flex;
  width: 1080px;
  margin-top: 96px;
  align-items: center;
  justify-content: space-between;
}
</style>
