
<script>
import AppNav from './components/AppNav.vue';
import MainContent from './components/MainContent.vue';
import AppIconsBar from './components/AppIconsBar.vue';

export default {
  components: {
    AppNav,
    MainContent,
    AppIconsBar
  }
}

</script>

<template>

  <AppNav></AppNav>

  <MainContent></MainContent>

  <AppIconsBar></AppIconsBar>

</template>

<style lang="scss">

@use './styles/general' as *;

</style>