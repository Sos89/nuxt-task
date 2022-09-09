<template>
  <v-container>
    <v-row>
      <v-col cols="12" sm="8" md="6">
        <form1099-n-e-c/>
      </v-col>
    </v-row>
  </v-container>
</template>
<script>
import form1099NEC from "~/components/forms/Form-1099-NEC";
export default {
  components: {form1099NEC}
}
</script>
