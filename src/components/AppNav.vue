
<script>

export default {
    name: 'AppNav',

    data() {
        return {
            links: ['Characters', 'Comics', 'Movies', 'TV', 'Games', 'Collectibles', 'Videos', 'Fans', 'news', 'Shop'],

            activeLinkIndex: 1,
        }
    }
}

</script>

<template>
    
    <nav>

        <div class="container">

            <img src="/img/dc-logo.png" alt="logo DC">
    
            <ul>
                <li v-for="(currentLink, index) in links" :class="activeLinkIndex == index ? 'active' : ''">
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