
<script>
import AppIconsBar from './AppIconsBar.vue';

export default {
    name: 'MainContent',

    components: {
        AppIconsBar
    },

    data() {

        return {
        }
    }
}

</script>

<template>
    
    <main>

        <div class="container">

            <div>
                --> Content goes here <--
            </div>

        </div>

    </main>

    <AppIconsBar></AppIconsBar>

</template>

<style lang="scss">

main {
    
    color: white;
    padding: 50px 0px;
    font-size: 20px;
    font-weight: bold;
}

</style>