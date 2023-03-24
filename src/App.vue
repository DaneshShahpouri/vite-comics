<script>
import AppNavbar from './components/AppNavabar.vue';
import AppMain from './components/AppMain.vue';
import AppBlueIcon from './components/AppBlueIcon.vue';
import AppFooter from './components/AppFooter.vue';

export default {
  data() {
    return {

    }
  },

  components: {
    AppNavbar,
    AppMain,
    AppBlueIcon,
    AppFooter,
  }

}
</script>

<template>
  <div>
    <AppNavbar></AppNavbar>
    <AppMain></AppMain>
    <AppBlueIcon></AppBlueIcon>
    <AppFooter></AppFooter>
  </div>
</template>

<style scoped></style>
