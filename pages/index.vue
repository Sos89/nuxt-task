<template>
  <v-container>
    <v-row>
      <v-col cols="12" sm="8" md="6">
<!--        <form1099-n-e-c/>-->
<!--        <form1098/>-->
<!--        <form1098T/>-->
<!--        <form-w2/>-->
        <form1099B/>
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
import Form1099NEC from "~/components/forms/Form-1099-NEC";
import form1098 from "~/components/forms/Form-1098"
import form1098T from "~/components/forms/Form-1098-T"
import formW2 from "~/components/forms/Form-W-2"
import form1099B from "~/components/forms/Form-1099-B";
export default {
  name: 'IndexPage',
  components: {Form1099NEC, form1098, form1098T, formW2, form1099B},
}
</script>
