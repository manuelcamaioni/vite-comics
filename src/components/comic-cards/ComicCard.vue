<template>
    <div class="card">
        <div class="img-container">
            <img :src="propDataCard.thumb" alt="" />
            <div class="overlay"></div>
            <span class="price">{{ propDataCard.price }}</span>
            <span class="type-book">{{ propDataCard.type }}</span>
        </div>
        <h3 class="title">{{ propDataCard.series }}</h3>
    </div>
</template>

<script>
export default {
    props: {
        propDataCard: Object,
    },
    data() {
        return {};
    },
};
</script>

<style lang="scss" scoped>
div.card {
    width: calc(100% / 6 - 0.5rem);
    height: 350px;

    h3.title {
        color: white;
        text-transform: uppercase;
        font-size: 0.8rem;
    }
    div.img-container {
        width: 100%;
        height: 80%;
        margin-bottom: 1rem;
        position: relative;
        img {
            width: 100%;
            height: 100%;
            display: block;
            object-fit: cover;
            object-position: center;
        }
    }
}
div.overlay {
    position: absolute;
    background-color: black;
    opacity: 0.5;
    transition: opacity 0.5s ease-out;
    top: 0;
    bottom: 0;
    right: 0;
    left: 0;
}
div.card:hover div.overlay {
    opacity: 0;
}
.img-container .price {
    position: absolute;
    top: 5px;
    right: 5px;

    background-color: rgb(250, 106, 54);
    border-radius: 0.5rem;
    opacity: 0;
    padding: 0.1rem 0.5rem;
    transition: opacity 0.5s ease-out;
}
.img-container:hover .price {
    display: block;
    opacity: 1;
}

.img-container .type-book {
    position: absolute;
    top: 30px;
    right: 5px;

    background-color: rgb(250, 106, 54);
    border-radius: 0.5rem;
    opacity: 0;
    padding: 0.1rem 0.5rem;
    transition: opacity 0.5s ease-out;
}

.img-container:hover .type-book {
    display: block;
    opacity: 1;
}
</style>
