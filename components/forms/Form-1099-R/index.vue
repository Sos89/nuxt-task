<template>
  <v-app class="bg">
    <v-container fluid class="container">
      <v-row cols="12">
        <h2 class="paragraph">2021 Form 1099-R</h2>
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
              label="Gross distribution"
              :styling="inputStyle"
            />
            <inputIndex
              label="Taxable amount"
              :styling="inputStyle"
            />
          </v-row>

          <v-row class="row">
            <div class="checkbox">
              <checkbox
                checkbox-label="Taxable amount not determined"
              />
            </div>
            <div class="checkbox">
              <checkbox
                checkbox-label="Total distribution"
              />
            </div>
          </v-row>

          <v-row class="row">
            <inputIndex
              label="Capital gain (included in box 2a)"
              :styling="inputStyle"
            />
            <inputIndex
              label="Federal income tax withheld"
              :styling="inputStyle"
            />
          </v-row>

          <v-row>
            <div class="row_state">
              <inputIndex
                label="Employee contributions/ Designated Roth contributions or insurance premiums"
                :styling="addressInput"
              />
            </div>
          </v-row>

          <v-row class="row">
            <inputIndex
              label="Net unrealized appreciation in employer's securities"
              :styling="inputStyle"
            />
            <inputIndex
              label="Distribution code(s)"
              :styling="inputStyle"
            />
          </v-row>

          <v-row class="row">
            <div class="checkbox">
              <checkbox
                checkbox-label="IRA/SEP/SIMPLE"
              />
            </div>
          </v-row>

          <v-row class="row">
            <inputIndex
              label="Other $"
              :styling="inputStyle"
            />
            <inputIndex
              label="Your percentage of total distribution"
              :styling="inputStyle"
            />
          </v-row>

          <v-row class="row">
            <inputIndex
              label="Total employee contributions"
              :styling="inputStyle"
            />
            <inputIndex
              label="State tax withheld"
              :styling="inputStyle"
            />
          </v-row>

          <v-row class="row">
            <selects
              label="State"
              :stylings="inputStyle"
            />
            <inputIndex
              label="Payer's state no."
              :styling="inputStyle"
            />
          </v-row>

          <v-row class="row">
            <inputIndex
              label="State distribution"
              :styling="inputStyle"
            />
            <inputIndex
              label="Local tax withheld"
              :styling="inputStyle"
            />
          </v-row>

          <v-row class="row">
            <inputIndex
              label="Name of locality"
              :styling="inputStyle"
            />
            <inputIndex
              label="Local distribution"
              :styling="inputStyle"
            />
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
        'border-radius': '10px',
        'background': 'withe'
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
  width: 100% !important;
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
</style>

