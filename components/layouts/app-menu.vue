<template>
  <div>
    <icon-menu
      title="Dashboard"
      icon="mdi-view-dashboard"
      class="dashboard"
    />
    <icon-menu
      title="Payers"
      icon="fa-solid fa-people-group"
    />
    <dropdown
      dropdown-title="Filings"
      dropdown-icon="fa-regular fa-folder-open"
      dropdown="fa-solid fa-caret-down"
      :filings="{'Field Forms': '/field/forms', 'Start Filing': 'start/filing', 'In Progress': '/progress', 'My Cart': '/cart'}"
    />
    <dropdown
      dropdown-icon="fa-solid fa-chart-column"
      dropdown-title="Reports"
      dropdown="fa-solid fa-caret-down"
      :filings="{
      '2021 Form 1099-NEC': '/form1099nec',
      'Form 1098': '/form1098',
      'Form 1098-T': '/form1098t',
       'Form W-2': '/formW2',
       'Form 1099-B': '/form1099b',
       'Form 1099-C': '/form1099c',
       'Form 1099-INT': '/form1099int',
       'Form 1099-R': '/form1099r',
       'Form 1099-DIV': '/form1099div',
       'Form 1099-S': '/form1099s',
       'Form 1042-S': '/form1042s',
    }"
    />
  </div>
</template>

<script>
import IconMenu from "~/components/menu/iconMenu";
import dropdown from "~/components/dropdown";

export default {
  name: "app-menu",
  components: {
    IconMenu,
    dropdown
  },
}
</script>

<style scoped>
.dashboard{
  margin-top: 26px;
}
</style>
