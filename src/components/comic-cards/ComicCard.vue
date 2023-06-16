<template>
    <div class="card">
        <div class="img-container">
            <img :src="propDataCard.thumb" alt="" />
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
        img {
            width: 100%;
            height: 100%;
            display: block;
            object-fit: cover;
            object-position: center;
        }
    }
}
</style>
