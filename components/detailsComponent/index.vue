<template>
<v-container>
  <v-row cols="12">
    <h2 class="paragraph">2021 Form 1042-S</h2>
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
</v-container>
</template>
<script>
import selects from "~/components/selects";
import detailsIndex from "~/components/details";
import inputIndex from "~/components/inputs";
export default {
  name: 'index',
  components: {
    selects,
    detailsIndex,
    inputIndex
  }
}
</script>
