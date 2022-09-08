<template>
  <div class="details">
    <span>{{ number }}.</span> <p>{{ text }} </p>
  </div>
</template>

<script>
export default {
  name: 'details-index',
  props: {
    number: Number,
    text: String
  }
}
</script>

<style scoped>
.details{
  width: 1080px;
  background: #FFFFFF;
  box-shadow: 2px 2px 10px rgba(210, 209, 223, 0.3);
  border-radius: 10px;
  display: flex;
  align-items: center;
  margin-top: 54px;
}
p{
  font-family: 'Questrial';
  font-style: normal;
  font-weight: 400;
  font-size: 16px;
  line-height: 20px;
  color: #6F6F6F;
  margin-top: 15px;
  margin-left: 15px;
}
span{
  font-family: 'Neue Haas Grotesk Text Pro';
  font-style: normal;
  font-weight: 700;
  font-size: 38px;
  line-height: 48px;
  text-align: center;
  color: #F4B42A;
  padding: 24px 24px 27px;
}
</style>
