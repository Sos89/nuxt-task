<template>
  <div>
    <v-hover v-slot="{ hover }" class="hover">
      <div @click="menuToggleer = !menuToggleer" class="dropdown-custom" :class="{ 'on-hover': hover }" :style="{ 'background-color': hover ? '#2B014C' : '#fff'}">
        <v-icon class="icon" :class="{ 'on-hover': hover }" :style="{ color: hover ? '#fff' : '#2B014C'}">{{dropdownIcon}}</v-icon>
        <span class="title" :class="{ 'on-hover': hover }" :style="{ color: hover ? '#fff' : '#2B014C'}">{{dropdownTitle}}</span>
        <v-icon class="dropdown-icon" :class="{ 'on-hover': hover }" :style="{ color: hover ? '#fff' : '#2B014C'}">{{dropdown}}</v-icon>
      </div>
    </v-hover>
    <div class="dropdown-menu" v-if="menuToggleer">
      <ul class="ul" v-for="(value, key, index) in filings">
        <li> <nuxt-link class="link" :to="value">{{key}}</nuxt-link></li>
      </ul>
    </div>
  </div>
</template>

<script>
export default {
  name: "index",
  data () {
    return {
      menuToggleer: false
    }
  },
  props: {
    dropdownTitle: String,
    dropdownIcon: String,
    dropdown: String,
    item: String,
    filings: Object
  }
}
</script>

<style scoped>
.dropdown-custom{
  cursor: pointer;
  color: #2B014C;
  padding-left: 24px;
  width: calc(100% - 16px);
  border-top-right-radius: 10px;
  border-bottom-right-radius: 10px;
  height: 56px;
  font-family: 'Neue Haas Grotesk Text Pro';
  font-style: normal;
  font-weight: 400;
  font-size: 18px;
  line-height: 22px;
  display: flex;
  align-items: center;
  color: #2B014C;
}
.ul{
  margin-left: 50px;
  cursor: pointer;
}
/*li :hover{*/
/*  background: #2B014C;*/
/*  color: #E5E5E5;*/
/*}*/
.dropdown-menu{
  color: #2B014C;
}
.icon{
  margin-right: 16px;
}
ul{
  list-style: none;
}
.dropdown-icon{
  font-size: 16px;
  width: calc(100% - 10px);
  margin-right: auto;
}
.link{
  font-family: 'Neue Haas Grotesk Text Pro';
  font-style: normal;
  font-weight: 400;
  font-size: 16px;
  line-height: 20px;
  display: flex;
  align-items: center;
  color: rgba(0, 0, 0, 0.7);
  text-decoration: none;
}
</style>
