
<script>

export default {

    name: 'ComicItem',

    props: {
        cardName: String,
        cardImage: String,
        cardPrice: String,
        cardType: String
    },

    data() {

        return {
        }
    }
}

</script>

<template>

    <div class="card">

        <div class="image">

            <img :src="cardImage" :alt="cardName">

            <div class="info">
    
                <h4>
                    <span>{{ cardType }}</span>
                </h4>
        
                <h4>
                    <span>{{ cardPrice }}</span>
                </h4>
            </div>
        </div>

        <h3>
            {{ cardName }}
        </h3>


    </div>

</template>

<style lang="scss">

.card {

    width: calc(100% / 6 - 25px / 6 * 5);

    &:hover {
        cursor: pointer;
    }

    &:hover .image .info {
        opacity: 1;
    }

    .image {

        position: relative;
        margin-bottom: 10px;

        
        img {
            width: 100%;
            aspect-ratio: 1 / 1;
            object-fit: cover;
            object-position: top;
        }
        
        .info {
            position: absolute;
            right: 0;
            bottom: 0;
            padding: 10px;
            text-align: right;
            opacity: 0;
            transition: .2s ease;

            h4 {

                font-size: 12px;
                span {
                    display: inline-block;
                    background-color: rgba(0, 0, 0, 0.514);
                    padding: 0px 4px;
                }
            }
        }
    }


    h3 {
        font-size: 12px;
        text-transform: uppercase;
    }

}

</style>