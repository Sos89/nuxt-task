<template>
      <v-hover v-slot="{ hover }" class="hover">
        <div class="manu" :class="{ 'on-hover': hover }" :style="{ 'background-color': hover ? '#2B014C' : '#fff'}">
            <v-icon class="icon" :class="{ 'on-hover': hover }" :style="{ color: hover ? '#fff' : '#2B014C'}">{{icon}}</v-icon>
             <span class="title" :class="{ 'on-hover': hover }" :style="{ color: hover ? '#fff' : '#2B014C'}">{{title}}</span>
        </div>
      </v-hover>
</template>

<script>
export default {
  name: "iconMenu",
  props: {
    title: String,
    icon: String
  },
}
</script>

<style scoped>
.manu{
  width: calc(100% - 16px);
  display: flex;
  flex-direction: row;
  align-items: center;
  height: 56px!important;
  padding-left: 24px;
  margin-right: 16px;
  border-top-right-radius: 10px!important;
  border-bottom-right-radius: 10px!important;
  cursor: pointer;
}
.title{
  font-family: 'Neue Haas Grotesk Text Pro';
  font-style: normal;
  font-weight: 400;
  font-size: 18px;
  line-height: 22px;
  display: flex;
  align-items: center;
  color: #2B014C;
  margin-left: 16px;
}
</style>
