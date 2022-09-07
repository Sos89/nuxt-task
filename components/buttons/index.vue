<template>
    <v-btn
      :color="color"
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
    color: String
  }
}
</script>
