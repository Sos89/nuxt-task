<template>
  <v-app class="bg">
    <v-container fluid class="container">
      <v-row cols="12">
        <h2 class="paragraph">2021 Form 1099-DIV</h2>
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
              label="1a Total ordinary dividends"
              :styling="inputStyle"
            />
            <inputIndex
              label="1b Qualified dividends"
              :styling="inputStyle"
            />
          </v-row>

          <v-row class="row">
            <inputIndex
              label="2a Total capital gain distr."
              :styling="inputStyle"
            />
            <inputIndex
              label="2b Unrecap. Sec. 1250 gain"
              :styling="inputStyle"
            />
          </v-row>

          <v-row class="row">
            <inputIndex
              label="2c Section 1202 gain"
              :styling="inputStyle"
            />
            <inputIndex
              label="2d Collectibles (28%) gain"
              :styling="inputStyle"
            />
          </v-row>

          <v-row class="row">
            <inputIndex
              label="2e Section 897 Ordinary Dividends"
              :styling="inputStyle"
            />
            <inputIndex
              label="2f Section 897 Capital Gain"
              :styling="inputStyle"
            />
          </v-row>

          <v-row class="row">
            <inputIndex
              label="3 Non dividend distributions"
              :styling="inputStyle"
            />
            <inputIndex
              label="4 Federal income tax withheld"
              :styling="inputStyle"
            />
          </v-row>

          <v-row class="row">
            <inputIndex
              label="5 Section 199A dividends"
              :styling="inputStyle"
            />
            <inputIndex
              label="6 Investment expenses"
              :styling="inputStyle"
            />
          </v-row>

          <v-row class="row">
            <inputIndex
              label="Foreign tax paid"
              :styling="inputStyle"
            />
            <inputIndex
              label="Foreign country or U.S. possession"
              :styling="inputStyle"
            />
          </v-row>

          <v-row class="row">
            <inputIndex
              label="Cash liquidation distributions"
              :styling="inputStyle"
            />
            <inputIndex
              label="Noncash liquidation distributions"
              :styling="inputStyle"
            />
          </v-row>

          <v-row class="row">
            <inputIndex
              label="11 Exempt-interest dividends"
              :styling="inputStyle"
            />
            <inputIndex
              label="12 Specified private activity bond interest dividends"
              :styling="inputStyle"
            />
          </v-row>

          <v-row class="row">
            <selects
              label="State"
              :stylings="inputStyle"
            />
            <inputIndex
              label="State identification no."
              :styling="inputStyle"
            />
          </v-row>

          <v-row class="row">
            <div class="row_state">
              <inputIndex
                label="State identification no."
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

