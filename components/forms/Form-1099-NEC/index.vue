<template>
  <v-app class="bg">
    <v-container fluid class="container">
        <v-row cols="12">
          <h2 class="paragraph">2021 Form 1099-NEC</h2>
        </v-row>
        <v-row cols="12" style="border: 2px solid; margin-top: 108px">
          <v-col>
            <h2 class="payer">Payer Details</h2>
          </v-col>
          <v-col>
            <v-row class="select_payer">
               <selects
                 :stylings="customStyle"
               />
               <index-button
                 button="+ Add Payer"
                 color="warning"
               />
            </v-row>
          </v-col>
        </v-row>
    </v-container>
  </v-app>
</template>

<script>
import selects from "~/components/selects";
import IndexButton from "~/components/buttons";
export default {
  name: "indexComponent",
  components: {IndexButton, selects},
  data(){
    return {
      customStyle: {
        'width': '200px',
        'height': '48px',
        'margin-right': '8px'
      }
    }
  }
}
</script>

<style scoped>
  .bg{
    background: #E5E5E5;
    width: 1640px;
    padding-left: 280px;
    padding-right: 280px;
  }
  .container{
  }
  .paragraph{
    font-family: 'Neue Haas Grotesk Text Pro';
    font-style: normal;
    font-weight: 700;
    font-size: 30px;
    line-height: 38px;
    color: #000000;
    margin-top: 154px;
  }
  .payer{
    font-family: 'Neue Haas Grotesk Text Pro';
    font-style: normal;
    font-weight: 400;
    font-size: 20px;
    line-height: 24px;
    color: #000000;
  }
</style>
