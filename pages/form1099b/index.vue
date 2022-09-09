<template>
  <v-container>
    <v-row>
      <v-col cols="12" sm="8" md="6">
        <form1099-b/>
      </v-col>
    </v-row>
  </v-container>
</template>
<script>
import form1099B from "~/components/forms/Form-1099-B";
export default {
  components: {form1099B}
}
</script>
