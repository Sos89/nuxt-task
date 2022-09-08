<template>
  <div>
<!--    <v-select-->
<!--      :style="getStyle"-->
<!--      :items="items"-->
<!--      label="Outlined style"-->
<!--      dense-->
<!--      outlined-->
<!--    ></v-select>-->
    <v-autocomplete
      :items="items"
      :style="getStyle"
      cache-items
      flat
      dense
      :label="label"
      outlined
    ></v-autocomplete>
  </div>
</template>
<script>
export default {
  name: "index-select",
  data () {
    return {
      toggleer: false
    }
  },
  props: {
    items: Object,
    stylings: Object,
    label: String
  },
  computed: {
    getStyle() {
      return this.stylings;
    }
  }
}
</script>
