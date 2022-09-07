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
    />
    <dropdown
      dropdown-icon="fa-solid fa-chart-column"
      dropdown-title="Reports"
      dropdown="fa-solid fa-caret-down"
      :filings="{'Login': '/login', 'Register': 'register', 'About': '/about'}"
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
