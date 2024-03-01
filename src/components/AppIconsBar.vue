
<script>

export default {
    name: 'AppIconsBar',

    data() {
        return {
            icons: [
                {
                    image: '/img/buy-comics-digital-comics.png',
                    text: 'Digital Comics'
                },
                {
                    image: '/img/buy-comics-merchandise.png',
                    text: 'DC Merchandise'
                },
                {
                    image: '/img/buy-comics-subscriptions.png',
                    text: 'Subscription'
                },
                {
                    image: '/img/buy-comics-shop-locator.png',
                    text: 'Comic Shop Locator'
                },
                {
                    image: '/img/buy-dc-power-visa.svg',
                    text: 'DC Power Visa'
                }
            ]
        }
    }
}

</script>

<template>

    <section class="icon-bar">

        <div class="container">
    
            <div class="row">
                
                <div class="col" v-for="(currentIcon, index) in icons">
                    <img :src="currentIcon.image" :alt="'immagine  ' + (index + 1)">
                    <div class="text">
                        {{ currentIcon.text }}
                    </div>
                </div>
            </div>
    
        </div>

    </section>

</template>

<style lang="scss">

@use '../styles/variables' as *;

.icon-bar {

    background-color: $primary-bg-color;


    .row {
        display: flex;
        justify-content: space-between;
        padding: 50px;

        .col {

            display: flex;
            align-items: center;
            gap: 18px;
            color: white;
            font-size: 12px;
            text-transform: uppercase;

            img {
                height: 55px;
            }

            &:last-of-type img {
                width: 55px;
                height: auto;
            }
        }


    }
}

</style>