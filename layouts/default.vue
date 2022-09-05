<template>
  <v-app>
    <app-bar></app-bar>
    <app-manu></app-manu>
  </v-app>
</template>

<script>
import AppBar from "~/components/layouts/app-bar";
import AppManu from "~/components/layouts/app-manu";
export default {
  name: 'DefaultLayout',
  components: {AppManu, AppBar},
}
</script>
<style>
.theme--dark.v-application{
  background: #ffffff;
}
</style>
