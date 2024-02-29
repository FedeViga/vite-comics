
<script>
import AppNav from './components/AppNav.vue';
import MainContent from './components/MainContent.vue';

export default {
  components: {
    AppNav,
    MainContent,
  }
}

</script>

<template>

  <AppNav></AppNav>

  <MainContent></MainContent>

</template>

<style lang="scss">

@use './styles/general' as *;

</style>