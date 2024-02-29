
<script>
import AppNav from './components/AppNav.vue';
import MainContent from './components/MainContent.vue';
import AppFooter from './components/AppFooter.vue';

export default {
  components: {
    AppNav,
    MainContent,
    AppFooter
  }
}

</script>

<template>

  <AppNav></AppNav>

  <MainContent></MainContent>

  <AppFooter></AppFooter>

</template>

<style lang="scss">

@use './styles/general' as *;

</style>