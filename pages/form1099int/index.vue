<template>
  <v-container>
    <v-row>
      <v-col cols="12" sm="8" md="6">
        <form1099-i-n-t/>
      </v-col>
    </v-row>
  </v-container>
</template>
<script>
import form1099INT from "~/components/forms/Form-1099-INT";
export default {
  components: {form1099INT}
}
</script>
