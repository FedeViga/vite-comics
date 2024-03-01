
<script>
import AppIconsBar from './AppIconsBar.vue';
import AppJumbo from './AppJumbo.vue';

export default {
    name: 'MainContent',

    components: {
        AppIconsBar,
        AppJumbo
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
        
        <AppIconsBar></AppIconsBar>

    </main>

</template>

<style lang="scss">

</style>