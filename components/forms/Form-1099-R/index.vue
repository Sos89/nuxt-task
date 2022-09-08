<template>
  <v-app class="bg">
    <v-container fluid class="container">
      <v-row cols="12">
        <h2 class="paragraph">2021 Form 1099-B</h2>
      </v-row>

      <v-row cols="12" style="margin-top: 108px">
        <v-col cols="6">
          <h2 class="payer">Payer Details</h2>
        </v-col>

        <v-col cols="6">
          <v-row class="d-flex justify-end select_payer">
            <selects
              :stylings="customStyle"
              label="Select Payer"
            />
            <index-button
              button="+ Add Payer"
              color="#F4B42A"
            />
          </v-row>
        </v-col>
      </v-row>
      <v-row>
        <details-index
          number = 1
          text="Next, select a previously entered recipient or choose to add a new recipient."
        />
      </v-row>
      <v-row>
        <div class="rec-details">
          <h2 class="payer">Recipient Details</h2>
          <selects
            :stylings="customStyle"
            label="Select Payer"
          />
        </div>
      </v-row>
      <v-row>
        <details-index
          number = 2
          text="Next, select a previously entered recipient or choose to add a new recipient."
        />
      </v-row>

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
export default {
  name: "index",
  components: {
    IndexButton,
    selects,
    detailsIndex,
    income,
    inputIndex,
    checkbox
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
.paragraph{
  font-family: 'Neue Haas Grotesk Text Pro';
  font-style: normal;
  font-weight: 700;
  font-size: 30px;
  line-height: 38px;
  color: #000000;
  margin-top: 154px;
  margin-right: auto;
}
.payer{
  font-family: 'Neue Haas Grotesk Text Pro';
  font-style: normal;
  font-weight: 400;
  font-size: 20px;
  line-height: 24px;
  color: #000000;
}
.rec-details{
  display: flex;
  width: 1080px;
  margin-top: 96px;
  align-items: center;
  justify-content: space-between;
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

