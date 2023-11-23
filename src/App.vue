<script>
import AppHeader from './components/AppHeader.vue';
import AppContent from './components/AppContent.vue';
import AppMain from './components/AppMain.vue';
import AppFooter from './components/AppFooter.vue';
import AppObjects from './components/AppObjects.vue';

export default {
  components: {
    AppHeader,
    AppContent,
    AppMain,
    AppFooter,
    AppObjects
},
};
</script>

<template>
  <AppHeader />
  <AppContent />
  <AppObjects/>
  <AppMain />
  <AppFooter />
</template>

<style lang="scss">
@use "./style/general.scss"
</style>
