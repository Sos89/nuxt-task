<template>
  <div class="app_bar_div">
    <v-container fluid>
      <v-row>
        <v-col cols="6" class="logo-div">
          <v-img
            src="/image/e.png"
            max-height="32"
            max-width="38"
          ></v-img>
        </v-col>
        <v-row cols="6" align="center" margin="right" justify="end">
          <div class="app_select_div">
            <v-img
              src="/image/Rectangle-30.png"
              max-height="32"
              max-width="38"
              class="img"
            >
            </v-img>
            <v-select
              v-model="e1"
              :items="states"
              width="202px"
              class="select"
              color="black"
              default="black"
            ></v-select>
          </div>
        </v-row>
      </v-row>
    </v-container>
  </div>
</template>
<script>
export default {
  name: 'app-bar',
  data(){
    return {
      e1: 'Florida',
      states: [
        'Alabama', 'Alaska', 'American Samoa', 'Arizona',
        'Arkansas', 'California', 'Colorado', 'Connecticut',
        'Delaware', 'District of Columbia', 'Federated States of Micronesia',
        'Florida', 'Georgia', 'Guam', 'Hawaii', 'Idaho',
        'Illinois', 'Indiana', 'Iowa', 'Kansas', 'Kentucky',
        'Louisiana', 'Maine', 'Marshall Islands', 'Maryland',
        'Massachusetts', 'Michigan', 'Minnesota', 'Mississippi',
        'Missouri', 'Montana', 'Nebraska', 'Nevada',
        'New Hampshire', 'New Jersey', 'New Mexico', 'New York',
        'North Carolina', 'North Dakota', 'Northern Mariana Islands', 'Ohio',
        'Oklahoma', 'Oregon', 'Palau', 'Pennsylvania', 'Puerto Rico',
        'Rhode Island', 'South Carolina', 'South Dakota', 'Tennessee',
        'Texas', 'Utah', 'Vermont', 'Virgin Island', 'Virginia',
        'Washington', 'West Virginia', 'Wisconsin', 'Wyoming',
      ],
    }
  }
}
</script>
<style scoped>
*{
  margin: 0;
  padding: 0;
}
.logo-div{
  margin: 16px 24px 16px 24px;
}
.app_bar_div{
    background: #FFFFFF;
    border-bottom: 1px solid rgba(0, 0, 0, 0.12);
    height: 64px;
  }
  .app_select_div{
    display: flex;
    align-items: center;
    width: 202px;
    height: 44px;
    border: 1px solid #EDEDED;
    border-radius: 10px;
    margin: 10px 24px 10px 24px;
  }
  .img{
    margin-right: 8px;
  }

</style>
