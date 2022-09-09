<template>
  <v-container>
    <v-row>
      <v-col cols="12" sm="8" md="6">
        <form1099-r/>
      </v-col>
    </v-row>
  </v-container>
</template>
<script>
import form1099R from "~/components/forms/Form-1099-R";
export default {
  components: {form1099R}
}
</script>
