<template>
  <v-app class="bg">
    <v-container fluid class="container">
      <v-row cols="12">
        <h2 class="paragraph">2021 Form W-2</h2>
      </v-row>
      <details-component/>
      <v-row>
        <income
          income="Income"
        />
      </v-row>

      <v-row>
        <v-form class="form">
          <v-row class="row">
            <inputIndex
              label="Wages, tips, other compensation"
              :styling="inputStyle"
            />
            <inputIndex
              label="Federal income tax withheld"
              :styling="inputStyle"
            />
          </v-row>
          <v-row class="row">
            <inputIndex
              label="Social security wages"
              :styling="inputStyle"
            />
            <inputIndex
              label="Social security tax withheld"
              :styling="inputStyle"
            />
          </v-row>
          <v-row class="row">
            <inputIndex
              label="Medicare wages and tips"
              :styling="inputStyle"
            />
            <inputIndex
              label="Medicare tax withheld"
              :styling="inputStyle"
            />
          </v-row>

          <v-row class="row">
            <inputIndex
              label=" Social security tips"
              :styling="inputStyle"
            />
            <inputIndex
              label="Allocated tips"
              :styling="inputStyle"
            />
          </v-row>
          <v-row class="row">
            <inputIndex
              label="Scholarships or grants"
              :styling="inputStyle"
            />
            <inputIndex
              label="Dependent care benefits"
              :styling="inputStyle"
            />
          </v-row>

          <v-row>
            <div class="checkbox">
              <checkbox
                checkbox-label="Statutory employee"
              />
            </div>
            <div class="checkbox">
              <checkbox
                checkbox-label="Retirement plan"
              />
            </div>
            <div class="checkbox">
              <checkbox
                checkbox-label="Third-party sick pay"
              />
            </div>
          </v-row>

          <v-row class="row">
            <inputIndex
              label="Code A"
              :styling="inputStyle"
            />
            <inputIndex
              label="Code B"
              :styling="inputStyle"
            />
          </v-row>

          <v-row class="row">
            <inputIndex
              label="Code C"
              :styling="inputStyle"
            />
            <inputIndex
              label="Code D"
              :styling="inputStyle"
            />
          </v-row>

          <v-row class="row">
            <inputIndex
              label="Amount A"
              :styling="inputStyle"
            />
            <inputIndex
              label="Amount B"
              :styling="inputStyle"
            />
          </v-row>

          <v-row class="row">
            <inputIndex
              label="Amount C"
              :styling="inputStyle"
            />
            <inputIndex
              label="Amount D"
              :styling="inputStyle"
            />
          </v-row>

          <v-row class="row">
            <inputIndex
              label="Other A"
              :styling="inputStyle"
            />
            <inputIndex
              label="Other B"
              :styling="inputStyle"
            />
          </v-row>

          <v-row class="row">
            <inputIndex
              label="Other C"
              :styling="inputStyle"
            />
            <inputIndex
              label="Other amount A"
              :styling="inputStyle"
            />
          </v-row>

          <v-row class="row">
            <inputIndex
              label="Other amount B"
              :styling="inputStyle"
            />
            <inputIndex
              label="Other amount C"
              :styling="inputStyle"
            />
          </v-row>
        </v-form>

        <v-row>
          <income
            income="State With holdings"
            incomeText="If your State is not part of the Combined Federal/State Filing program, you may check to file State Tax information directly to that State. A rate of $1.00 per form will be added to your cart. Supported states are: DC, GA, IL, KS, MI, NC, ND, VA, VT, WI."
          />
        </v-row>

        <v-form class="form">
          <v-row class="row">
            <selects
              :stylings="inputStyle"
              label="State"
            />
            <selects
              :stylings="inputStyle"
              label="State"
            />
          </v-row>
          <v-row class="row">
            <inputIndex
              label="Employer’s state ID number"
              :styling="inputStyle"
            />
            <inputIndex
              label="Employer’s state ID number"
              :styling="inputStyle"
            />
          </v-row>
          <v-row class="row">
            <inputIndex
              label="State wages, tips, etc."
              :styling="inputStyle"
            />
            <inputIndex
              label="State wages, tips, etc."
              :styling="inputStyle"
            />
          </v-row>
          <v-row class="row">
            <inputIndex
              label="State income tax"
              :styling="inputStyle"
            />
            <inputIndex
              label="State income tax"
              :styling="inputStyle"
            />
          </v-row>
          <v-row class="row">
            <inputIndex
              label="Local wages, tips, etc."
              :styling="inputStyle"
            />
            <inputIndex
              label="Local wages, tips, etc."
              :styling="inputStyle"
            />
          </v-row>
          <v-row class="row">
            <inputIndex
              label="Locality name"
              :styling="inputStyle"
            />
            <inputIndex
              label="Locality name"
              :styling="inputStyle"
            />
          </v-row>
        </v-form>
        <v-row>
          <h2 class="mDetails">Misc. Details</h2>
        </v-row>
        <v-form class="form">
          <v-row class="row">
            <inputIndex
              label="Kind of payer"
              :styling="inputStyle"
            />
            <inputIndex
              label="Terminating Business"
              :styling="inputStyle"
            />
          </v-row>
          <v-row>
            <div class="checkbox">
              <checkbox
                checkbox-label="Check this box if the amount in box 1 includes amounts for an academic period beginning January–March 2022"
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
    detailsComponent,
  },
  data(){
    return {
      customStyle: {
        'width': '200px',
        'height': '48px',
        'margin-right': '8px',
        'border-radius': '10px'
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
        'font-weight': 700,
        'font-size': '16px',
        'line-height': '20px',
        'color': 'white',
        'flex': 'none',
        'order': 0,
        'flex-grow': 0,
      },
      addressInput: {
        'width': '100%',
        'border-radius': '10px'
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
  margin-right: 10px;
}
.checkbox{
  width: 100%;
  margin-left: 10px;
  margin-bottom: 15px;
}
.btn{
  margin-bottom: 32px;
}
.mDetails{
  font-family: 'Neue Haas Grotesk Text Pro';
  font-style: normal;
  font-weight: 400;
  font-size: 20px;
  line-height: 24px;
  color: #000000;
  margin-right: auto;
  margin-left: 10px;
  margin-top: 60px;
}
</style>

