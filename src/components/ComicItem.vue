
<script>

export default {

    name: 'ComicItem',

    props: {
        cardName: String,
        cardImage: String
    },

    data() {

        return {
        }
    }
}

</script>

<template>

    <div class="card">

        <img :src="cardImage" :alt="cardName">

        <h3>
            {{ cardName }}
        </h3>

    </div>

</template>

<style lang="scss">

.card {
    width: calc(100% / 6 - 25px / 6 * 5);

    img {
        width: 100%;
        aspect-ratio: 1 / 1;
        object-fit: cover;
        object-position: top;
        margin-bottom: 10px;
    }

    h3 {
        font-size: 12px;
        text-transform: uppercase;
    }
}

</style>