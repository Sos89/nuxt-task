<template>
  <v-app class="bg">
    <v-container fluid class="container">
      <v-row cols="12">
        <h2 class="paragraph">2021 Form 1099-S</h2>
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
              label="1 Date of closing"
              :styling="inputStyle"
              icon="fa-calendar"
            />
            <inputIndex
              label="2 Gross proceeds"
              :styling="inputStyle"
            />
          </v-row>
          <v-row class="row">
            <inputIndex
              label="3 Address (including city, state, and ZIP code) or legal description"
              :styling="inputStyle"
            />
            <inputIndex
              label="6 Buyer’s part of real estate tax"
              :styling="inputStyle"
            />
          </v-row>
          <v-row>
            <div class="checkbox">
              <checkbox
                checkbox-label="Check here if the transferor received or will receive property or services as part of the consideration"
              />
            </div>
            <div class="checkbox">
              <checkbox
                checkbox-label="Check here if the transferor is a foreign person (nonresident alien, foreign partnership, foreign estate, or foreign trust)"
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
  name: "indexComponent",
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
.checkbox{
  width: 100%;
  margin-left: 10px;
  margin-bottom: 15px;
}
.btn{
  margin-bottom: 32px;
}
</style>
