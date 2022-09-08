<template>
  <div>
    <v-text-field
      :label="label"
      :style="getStyle"
      outlined
      dense
    ></v-text-field>
  </div>
</template>
<script>
export default {
  name: 'input-index',
  props: {
    label: String,
    styling: Object
  },
  computed: {
    getStyle() {
      return this.styling;
    }
  }
}
</script>
