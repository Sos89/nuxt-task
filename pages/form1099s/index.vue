<template>
  <v-container>
    <v-row>
      <v-col cols="12" sm="8" md="6">
        <form1099-s/>
      </v-col>
    </v-row>
  </v-container>
</template>
<script>
import form1099S from "~/components/forms/Form-1099-S";
export default {
  components: {form1099S}
}
</script>
