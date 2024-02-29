
<script>
import AppNav from './components/AppNav.vue';
import MainContent from './components/MainContent.vue';
import AppIconsBar from './components/AppIconsBar.vue';
import AppFooter from './components/AppFooter.vue';

export default {
  components: {
    AppNav,
    MainContent,
    AppIconsBar,
    AppFooter
  }
}

</script>

<template>

  <AppNav></AppNav>

  <MainContent></MainContent>

  <AppIconsBar></AppIconsBar>

  <AppFooter></AppFooter>

</template>

<style lang="scss">

@use './styles/general' as *;

</style>