<template>
  <v-navigation-drawer permanent light>
    <v-hover v-slot="{ hover }">
      <div class="dashboard" :class="{ 'on-hover': hover }" :style="{ 'background-color': hover ? '#2B014C' : '#fff'}">
        <nuxt-link to="#" :class="{ 'on-hover': hover }" :style="{ color: hover ? '#fff' : '#2B014C'}">
          <v-icon class="icon" :class="{ 'on-hover': hover }" :style="{ color: hover ? '#fff' : '#2B014C'}">mdi-view-dashboard</v-icon>
          Dashboard
        </nuxt-link>
      </div>
    </v-hover>
    <v-hover v-slot="{ hover }">
      <div class="payers" :class="{ 'on-hover': hover }" :style="{ 'background-color': hover ? '#2B014C' : '#fff'}">
        <nuxt-link to="#" :class="{ 'on-hover': hover }" :style="{ color: hover ? '#fff' : '#2B014C'}">
          <v-icon class="icon" :class="{ 'on-hover': hover }" :style="{ color: hover ? '#fff' : '#2B014C'}">mdi-view-payers</v-icon>
          Payers
        </nuxt-link>
      </div>
    </v-hover>

  </v-navigation-drawer>
</template>

<script>
export default {
  name: "app-manu",
  data () {
    return {
    }
  },
}
</script>

<style scoped>
nuxt-link{
  text-decoration: none!important;
  margin-right: 16px;
}
.dashboard, .payers{
  display: flex;
  flex-direction: row;
  align-items: center;
  width: 2643px!important;
  height: 56px!important;
  padding-left: 24px;
}
.icon{
  margin-right: 16px;
}
</style>
