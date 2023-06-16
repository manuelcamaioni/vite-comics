<template>
    <div class="card">
        <div class="img-container">
            <img :src="propDataCard.thumb" alt="" />
            <div class="overlay"></div>
            <div class="info-box">
                <span class="price">{{ propDataCard.price }}</span>
                <span class="type-book">{{ propDataCard.type }}</span>
            </div>
            <div class="abs-container"></div>
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

div.info-box {
    position: absolute;
    top: 0;
    right: 0;
    left: 0;
    z-index: 1;

    height: 50px;
    display: flex;
    justify-content: space-between;
    align-items: center;
}
.price,
.type-book {
    opacity: 0;

    padding: 0 0.3rem;
}

.type-book {
    text-transform: capitalize;
}

.abs-container {
    position: absolute;
    top: 0;
    right: 0;
    width: 0;
    height: 50px;
    background-color: orangered;

    transition: width 1.2s;
}

div.card:hover .abs-container {
    width: 100%;
}

div.card:hover .price,
div.card:hover .type-book {
    opacity: 1;
    transition: opacity 2s;
}
</style>
