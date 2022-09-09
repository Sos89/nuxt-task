<template>
  <v-app class="bg">
    <v-container fluid class="container">
      <v-row cols="12">
        <h2 class="paragraph">2021 Form 1099-NEC</h2>
      </v-row>
      <details-component/>
      <v-row>
        <income
          income="Income"
          incomeText="If your State is not part of the Combined Federal/State Filing program, you may check to file State Tax information directly to that State. A rate of $1.00 per form will be added to your cart. Supported states are: DC, GA, IL, KS, MI, NC, OR, RI, VA, VT, WI."
        />
      </v-row>
      <v-row>
        <v-form class="form">
         <v-row class="row">
             <inputIndex
               label="None employee compensation"
               :styling="inputStyle"
             />
             <inputIndex
               label="Federal income tax withheld"
               :styling="inputStyle"
             />
         </v-row>
          <v-row>
            <div class="checkbox">
              <checkbox
                checkbox-label="Payer made direct sales totaling $5,000 or more of consumer products to recipient for resale"
              />
            </div>
          </v-row>
         <v-row class="row">
             <inputIndex
               label="Federal income tax withheld"
               :styling="inputStyle"
             />
             <inputIndex
               label="State tax withheld"
               :styling="inputStyle"
             />
         </v-row>
         <v-row class="row">
           <selects
             :stylings="inputStyle"
             label="State"
           />
           <inputIndex
             label="Payer's state no."
             :styling="inputStyle"
           />
         </v-row>
         <v-row>
           <div class="row_state">
             <inputIndex
               label="State income"
               :styling="inputStyle"
             />
           </div>
         </v-row>
         <v-row class="row btn">
           <index-button
             button="Save"
             color="#F4B42A"
             :style="saveButton"
           />
           <index-button
             button="Cancel"
             color="white"
             :style="buttonStyl"
           />
         </v-row>

        </v-form>
      </v-row>

    </v-container>
  </v-app>
</template>

<script>
import selects from "~/components/selects";
import IndexButton from "~/components/buttons";
import detailsIndex from "~/components/details";
import income from "~/components/Income"
import inputIndex from "~/components/inputs";
import checkbox from "~/components/checkbox";
import detailsComponent from "~/components/detailsComponent";
export default {
  name: "index",
  components: {
    IndexButton,
    selects,
    detailsIndex,
    income,
    inputIndex,
    checkbox,
    detailsComponent
  },
  data(){
    return {
      customStyle: {
        'width': '200px',
        'height': '48px',
        'background': '#E5E5E5',
        'margin-right': '8px',
        'border-radius': '10px',
      },
      inputStyle: {
        'width': '508px',
        'border-radius': '10px'
      },
      buttonStyl: {
        'width': '508px',
        'font-family': 'Neue Haas Grotesk Text Pro',
        'font-style': 'normal',
        'font-weight': 400,
        'font-size': '16px',
        'line-height': '20px',
        'color': '#6F6F6F',
        'flex': 'none',
        'order': 0,
        'flex-grow': 0,
        'border': '1px solid #BFBFBF',
      },
      saveButton: {
        'width': '508px',
        'font-family': 'Neue Haas Grotesk Text Pro',
        'font-style': 'normal',
        'font-weight': 400,
        'font-size': '16px',
        'line-height': '20px',
        'color': 'white',
        'flex': 'none',
        'order': 0,
        'flex-grow': 0,
        'border': '1px solid #BFBFBF',
      },
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

  .form{
    background: #FFFFFF;
    box-shadow: 2px 2px 10px rgba(210, 209, 223, 0.3);
    border-radius: 10px;
    margin-top: 42px;
    padding: 36px 24px 36px 24px;
    display: flex;
    align-items: center;
    justify-content: center;
    flex-wrap: wrap;
    margin-bottom: 36px;
  }
  .row{
    display: flex;
    justify-content: space-around;
  }
  .row_state{
    width: 100%;
    margin-left: 10px;
  }
  .checkbox{
    width: 100%;
    margin-left: 10px;
    margin-bottom: 15px;
  }
.btn{
  margin-bottom: 32px;
}
</style>
