<template>
  <div>
    <v-checkbox
      v-model="checkbox"
      :label="checkboxLabel"
    ></v-checkbox>
  </div>
</template>

<script>
export default {
  name: "index",
  data(){
    return {
      checkbox: false
    }
  },
  props: {
    checkboxLabel: String
  }
}
</script>

<style scoped>

</style>
