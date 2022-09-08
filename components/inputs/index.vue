<template>
  <div>
    <v-text-field
      :label="label"
      :style="getStyle"
      :type="type"
      :append-icon="icon"
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
    styling: Object,
    type: String,
    icon: String
  },
  computed: {
    getStyle() {
      return this.styling;
    }
  }
}
</script>
