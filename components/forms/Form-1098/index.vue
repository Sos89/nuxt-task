<template>
  <v-app class="bg">
    <v-container fluid class="container">
      <v-row cols="12">
        <h2 class="paragraph">2021 Form 1098</h2>
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
              label="Mortgage interest received from payer(s)/borrower(s)"
              :styling="inputStyle"
            />
            <inputIndex
              label="Outstanding mortgage principal"
              :styling="inputStyle"
            />
          </v-row>
          <v-row class="row">
            <inputIndex
              label="Mortgage origination date"
              :styling="inputStyle"
              icon="fa-calendar"
            />
            <inputIndex
              label="State tax withheld"
              :styling="inputStyle"
            />
          </v-row>
          <v-row class="row">
            <inputIndex
              label="Mortgage insurance premiums"
              :styling="inputStyle"
            />
            <inputIndex
              label="Points paid on purchase of principal residence"
              :styling="inputStyle"
            />
          </v-row>
          <v-row>
            <div class="checkbox">
              <checkbox
                checkbox-label="If address of property securing mortgage is the same as PAYER’S/BORROWER’S address, check the box, or enter the address or description in box 8."
              />
            </div>
          </v-row>
          <v-row class="row">
            <div class="row_state">
              <inputIndex
                label="Address or description of property securing mortgage (see instructions)"
                :styling="addressInput"
              />
            </div>
            <div class="mr-auto data">
              <inputIndex
                label="Mortgage acquisition date"
                :styling="inputStyle"
                icon="fa-calendar"
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
        'font-weight': 400,
        'font-size': '16px',
        'line-height': '20px',
        'color': 'white',
        'flex': 'none',
        'order': 0,
        'flex-grow': 0,
        'border': '1px solid #BFBFBF',
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
.data{
  margin-left: 10px;
}
</style>
