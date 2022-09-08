<template>
  <div>
    <p class="income">{{ income }}</p>
    <p class="incomeText">{{ incomeText }}</p>
  </div>
</template>
<script>
export default {
  name: 'income-index',
  props: {
    income: String,
    incomeText: String
  }
}
</script>
<style scoped>
div{
  margin-top: 96px;
  width: 1080px;
}
.income{
  font-family: 'Neue Haas Grotesk Text Pro';
  font-style: normal;
  font-weight: 400;
  font-size: 20px;
  line-height: 24px;
  color: #000000;
}
.incomeText{
  font-family: 'Questrial';
  font-style: normal;
  font-weight: 400;
  font-size: 16px;
  line-height: 20px;
  color: #6F6F6F;
}
</style>
