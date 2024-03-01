
<script>

export default {
    name: 'AppNav',

    data() {
        return {
            links: ['Characters', 'Comics', 'Movies', 'TV', 'Games', 'Collectibles', 'Videos', 'Fans', 'news', 'Shop'],

            activeLinkIndex: 1,
        }

    },

    methods: {

        activeLink(index) {
            this.activeLinkIndex = index
        }

},
}

</script>

<template>
    
    <nav>

        <div class="container">

            <img src="/img/dc-logo.png" alt="logo DC">
    
            <ul>
                <li 
                    v-for="(currentLink, index) in links" 
                    :class="activeLinkIndex == index ? 'active' : ''"
                    @click="activeLink(index)"
                >
                    {{ currentLink }}
                </li>
            </ul>

        </div>

    </nav>

</template>

<style lang="scss">

@use '../styles/variables' as *;

nav {

    background-color: white;
    position: fixed;
    top: 0;
    width: 100%;
    z-index: 2;

    .container {

        display: flex;
        justify-content: space-between;
        padding: 20px 10px;

        img {
            width: 80px;
        }
    
        ul {
            display: flex;
            list-style-type: none;
            align-items: center;
            gap: 30px;
    
            li {
                position: relative;
                text-transform: uppercase;
                font-weight: bold;
                font-size: 12px;
                transition: .2s ease;

                &:hover {
                    cursor: pointer;
                    color: $primary-color;
                }

                &.active {
                    color: $primary-bg-color
                }
            
                &.active::before {
                    content: '';
                    position: absolute;
                    bottom: calc((-120px + 18px) / 2);
                    width: 100%;
                    height: 5px;
                    background-color: $primary-bg-color
                }
            }
        }
    
    }

}

</style>