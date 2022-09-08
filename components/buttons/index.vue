<template>
    <v-btn
      :color="color"
      :style="getStyle"
      dark
    >
     {{ button }}
    </v-btn>
</template>
<script>
export default {
  name: 'index-button',
  props: {
    button: String,
    color: String,
    styling: Object
  },
  computed:{
    getStyle(){
      return this.styling
    }
  }
}
</script>
