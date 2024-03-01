
<script>
import AppIconsBar from './AppIconsBar.vue';
import AppJumbo from './AppJumbo.vue';
import AppComics from './AppComics.vue';

export default {
    name: 'MainContent',

    components: {
        AppIconsBar,
        AppJumbo,
        AppComics
    },

    data() {

        return {
        }
    }
}

</script>

<template>

    <main>
        
        <AppJumbo></AppJumbo>

        <AppComics></AppComics>
        
        <AppIconsBar></AppIconsBar>

    </main>

</template>

<style lang="scss">

main {
    color: white;
    margin-top: 120px;
}

</style>