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
            <selects
              label="UNIQUE FORM IDENTIFIER"
              :stylings="inputStyle"
            />
            <inputIndex
              label="1 Income code"
              :styling="inputStyle"
            />
          </v-row>

          <v-row class="row">
            <inputIndex
              label="Chapter indicator"
              :styling="inputStyle"
            />
            <selects
              label="3a Exemption code"
              :stylings="inputStyle"
            />
          </v-row>

          <v-row class="row">
            <selects
              label="3b Tax rate"
              :stylings="inputStyle"
            />
            <selects
              label="4a Exemption code"
              :stylings="inputStyle"
            />
          </v-row>

          <v-row class="row">
            <selects
              label="4b Tax rate"
              :stylings="inputStyle"
            />
            <inputIndex
              label="5 Withholding allowance"
              :styling="inputStyle"
            />
          </v-row>

          <v-row class="row">
            <inputIndex
              label="6 Net income"
              :styling="inputStyle"
            />
            <inputIndex
              label="7a Federal tax withheld"
              :styling="inputStyle"
            />
          </v-row>

          <v-row class="row">
            <div class="row_state">
              <inputIndex
                label="Federal Tax Withheld Indicator"
                :styling="inputStyle"
              />
            </div>
          </v-row>

          <v-row>
            <div class="checkbox">
              <checkbox
                checkbox-label="7b Check if federal tax withheld was not deposited with the IRS because escrow procedures were applied (see instructions)"
              />
            </div>
            <div class="checkbox">
              <checkbox
                checkbox-label="7c Check if withholding occurred in subsequent year with respect to a partnership interest"
              />
            </div>
          </v-row>

          <v-row class="row">
            <div class="row_state">
              <selects
                label="8 Tax withheld by other agents"
                :styling="addressInput"
              />
            </div>

            <div class="row_state">
              <inputIndex
                label="9 Over withheld tax repaid to recipient pursuant to adjustment procedures (see instructions)"
                :styling="addressInput"
              />
            </div>

            <div class="row_state">
              <inputIndex
                label="11 Tax paid by withholding agent (amounts not withheld) (see instructions)"
                :styling="addressInput"
              />
            </div>
          </v-row>

          <v-row class="row">
            <selects
              label="12b Chapter 3 status code"
              :stylings="inputStyle"
            />
            <selects
              label="12c Chapter 4 status code"
              :stylings="inputStyle"
            />
          </v-row>

          <v-row class="row">
            <inputIndex
              label="12d Withholding Agent's Name 1"
              :styling="inputStyle"
            />
            <inputIndex
              label="Title/Department"
              :styling="inputStyle"
            />
          </v-row>

          <v-row class="row">
            <inputIndex
              label="Title/Department"
              :styling="inputStyle"
            />
            <inputIndex
              label="Contact Number"
              :styling="inputStyle"
            />
          </v-row>

          <v-row class="row">
            <div class="row_state">
              <inputIndex
                label="12e Withholding agent's Global Intermediary Identification Number (GIIN)"
                :styling="addressInput"
              />
            </div>
          </v-row>

          <v-row class="row">
            <inputIndex
              label="12f Country code"
              :styling="inputStyle"
            />
            <inputIndex
              label="12g Foreign taxpayer identification number, if any"
              :styling="inputStyle"
            />
          </v-row>

          <v-row class="row">
            <inputIndex
              label="12h Address 1 (number and street)"
              :styling="inputStyle"
            />
            <inputIndex
              label="12h Address 2 (number and street)"
              :styling="inputStyle"
            />
          </v-row>

          <v-row class="row">
            <inputIndex
              label="12i City or town"
              :styling="inputStyle"
            />
            <inputIndex
              label="12i State or province"
              :styling="inputStyle"
            />
          </v-row>

          <v-row class="row">
            <inputIndex
              label="12i Country"
              :styling="inputStyle"
            />
            <inputIndex
              label="12i ZIP or foreign postal code"
              :styling="inputStyle"
            />
          </v-row>

          <v-row class="row">
            <inputIndex
              label="13a Recipient's name"
              :styling="inputStyle"
            />
            <inputIndex
              label="13a Recipient's Last name"
              :styling="inputStyle"
            />
          </v-row>

          <v-row class="row">
            <selects
              label="13b Recipient's country code"
              :stylings="inputStyle"
            />
            <inputIndex
              label="13c Address(number and street) 1"
              :styling="inputStyle"
            />
          </v-row>

          <v-row class="row">
            <inputIndex
              label="13c Address(number and street) 2"
              :styling="inputStyle"
            />
            <inputIndex
              label="13d City or town"
              :styling="inputStyle"
            />
          </v-row>

          <v-row class="row">
            <inputIndex
              label="13d State or province"
              :styling="inputStyle"
            />
            <inputIndex
              label="13d Country"
              :styling="inputStyle"
            />
          </v-row>

          <v-row class="row">
            <inputIndex
              label="13d ZIP or foreign postal code"
              :styling="inputStyle"
            />
            <inputIndex
              label="13e Recipient's U.S.TIN, if any"
              :styling="inputStyle"
            />
          </v-row>

          <v-row>
            <div class="checkbox">
              <checkbox
                checkbox-label="Check the box before if this is QI-EIN, WP-EIN, or WT-EIN that has entered into a withholding agreement with the IRS"
              />
            </div>
          </v-row>

          <v-row class="row">
            <selects
              label="Recipient's Federal Identification Number Type"
              :stylings="inputStyle"
            />
            <selects
              label="13f Chapter 3 status code"
              :stylings="inputStyle"
            />
          </v-row>

          <v-row class="row">
            <inputIndex
              label="13h Recipient's GIIN"
              :styling="inputStyle"
            />
            <selects
              label="13j LOB code"
              :stylings="inputStyle"
            />
          </v-row>

          <v-row class="row">
            <inputIndex
              label="13l Recipient's date of birth"
              :styling="inputStyle"
            />
            <inputIndex
              label="14a Primary Withholding Agent's Name 1 (if applicable)"
              :styling="inputStyle"
            />
          </v-row>

          <v-row class="row">
            <inputIndex
              label="14a Primary Withholding Agent's Name 2 (if applicable)"
              :styling="inputStyle"
            />
            <inputIndex
              label="14b Primary Withholding Agent's EIN"
              :styling="inputStyle"
            />
          </v-row>

          <v-row>
            <div class="checkbox">
              <checkbox
                checkbox-label="15 Check if pro - rata basis reporting"
              />
            </div>
          </v-row>

          <v-row class="row">
            <inputIndex
              label="15a Intermediary or flow - through entity's EIN, if any"
              :styling="inputStyle"
            />
            <selects
              label="15b Chapter 3 status code"
              :stylings="inputStyle"
            />
          </v-row>

          <v-row class="row">
            <selects
              label="15c Chapter 4 status code"
              :stylings="inputStyle"
            />
            <inputIndex
              label="15d Intermediary or flow - through entity's Name"
              :styling="inputStyle"
            />
          </v-row>

          <v-row class="row">
            <inputIndex
              label="15e Intermediary or flow - through entity's GIIN"
              :styling="inputStyle"
            />
            <inputIndex
              label="15f Country code"
              :styling="inputStyle"
            />
          </v-row>

          <v-row class="row">
            <inputIndex
              label="15g Foreign tax identification number, if any"
              :styling="inputStyle"
            />
            <inputIndex
              label="15h Address (number and street)"
              :styling="inputStyle"
            />
          </v-row>

          <v-row class="row">
            <inputIndex
              label="15i City or town"
              :styling="inputStyle"
            />
            <selects
              label="15i State or province"
              :stylings="inputStyle"
            />
          </v-row>

          <v-row class="row">
            <selects
              label="15i Country"
              :stylings="inputStyle"
            />
            <inputIndex
              label="15i ZIP or foreign postal code"
              :styling="inputStyle"
            />
          </v-row>

          <v-row class="row">
            <inputIndex
              label="16a Payer's name"
              :styling="inputStyle"
            />
            <inputIndex
              label="16b Payer's TIN"
              :styling="inputStyle"
            />
          </v-row>

          <v-row class="row">
            <inputIndex
              label="16b Payer's TIN"
              :styling="inputStyle"
            />
            <selects
              label="16d Chapter 3 status code"
              :stylings="inputStyle"
            />
          </v-row>

          <v-row class="row">
            <selects
              label="16e Chapter 4 status code"
              :stylings="inputStyle"
            />
            <inputIndex
              label="17a State income tax withheld"
              :styling="inputStyle"
            />
          </v-row>

          <v-row class="row">
            <inputIndex
              label="17b Payer's state tax no."
              :styling="inputStyle"
            />
            <selects
              label="17c Name of state"
              :stylings="inputStyle"
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

