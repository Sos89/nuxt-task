<template>
  <div>
    <v-select
      :style="getStyle"
      :items="items"
      label="Outlined style"
      dense
      outlined
    ></v-select>
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
  },
  computed: {
    getStyle() {
      return this.stylings;
    }
  }
}
</script>
