<template>
  <v-container>
    <v-row>
      <v-col cols="12" sm="8" md="6">
        <form1099-c/>
      </v-col>
    </v-row>
  </v-container>
</template>
<script>
import form1099C from "~/components/forms/Form-1099-C";
export default {
  components: {form1099C}
}
</script>
