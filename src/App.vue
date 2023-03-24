<script>
import AppNavbar from './components/AppNavabar.vue';
import AppMain from './components/AppMain.vue';
import AppBlueIcon from './components/AppBlueIcon.vue';

export default {
  data() {
    return {

    }
  },

  components: {
    AppNavbar,
    AppMain,
    AppBlueIcon,
  }

}
</script>

<template>
  <div>
    <AppNavbar></AppNavbar>
    <AppMain></AppMain>
    <AppBlueIcon></AppBlueIcon>
  </div>
</template>

<style scoped></style>
