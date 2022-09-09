<template>
  <v-container>
    <v-row>
      <v-col cols="12" sm="8" md="6">
        <form1099-n-e-c/>
<!--        <form1098/>-->
<!--        <form1098T/>-->
<!--        <form-w2/>-->
<!--        <form1099B/>-->
<!--        <form1099-c/>-->
<!--        <form1099-i-n-t/>-->
<!--        <form1099R/>-->
<!--        <form1099-d-i-v/>-->
<!--        <form1099-s/>-->
<!--        <form1042S/>-->
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
import form1099C from "~/components/forms/Form-1099-C";
import form1099INT from "~/components/forms/Form-1099-INT";
import form1099R from "~/components/forms/Form-1099-R";
import form1099DIV from "~/components/forms/Form-1099-DIV";
import form1099S from "~/components/forms/Form-1099-S";
import form1042S from "~/components/forms/Form-1042-S";
export default {
  name: 'IndexPage',
  components: {
    Form1099NEC,
    form1098,
    form1098T,
    formW2,
    form1099B,
    form1099C,
    form1099INT,
    form1099R,
    form1099DIV,
    form1099S,
    form1042S
  },
}
</script>
