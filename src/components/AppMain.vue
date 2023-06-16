<template>
    <main>
        <div class="extended-wrapper bg-black">
            <div class="jumbo-container"></div>
            <div class="container">
                <AppComicsContainer />
            </div>
            <div class="extended-wrapper bg-primary">
                <div class="container d-flex items">
                    <div class="item-container d-flex align-center">
                        <img
                            src="../assets/vue-dc-comics-1/img/buy-comics-digital-comics.png"
                            alt="" />
                        <span>digital comics</span>
                    </div>
                    <div class="item-container d-flex align-center">
                        <img
                            src="../assets/vue-dc-comics-1/img/buy-comics-merchandise.png"
                            alt="" />
                        <span>Dc Merchandise</span>
                    </div>
                    <div class="item-container d-flex align-center">
                        <img
                            src="../assets/vue-dc-comics-1/img/buy-comics-shop-locator.png"
                            alt="" />
                        <span>Comic Shop Locator</span>
                    </div>
                    <div class="item-container d-flex align-center">
                        <img
                            src="../assets/vue-dc-comics-1/img/buy-comics-subscriptions.png"
                            alt="" />
                        <span>Subscriptions</span>
                    </div>
                    <div class="item-container d-flex align-center">
                        <img
                            src="../assets/vue-dc-comics-1/img/buy-dc-power-visa.svg"
                            alt="" />
                        <span>DC Power visa</span>
                    </div>
                </div>
            </div>
        </div>
    </main>
</template>

<script>
import AppComicsContainer from "./comic-cards/AppComicsContainer.vue";

export default {
    components: {
        AppComicsContainer,
    },
    data() {
        return {};
    },
};
</script>

<style lang="scss" scoped>
main {
    .extended-wrapper {
        width: 100%;
        .jumbo-container {
            height: 500px;
            width: 100%;
            background: url("../assets/vue-dc-comics-1/img/jumbotron.jpg");
        }

        .items {
            justify-content: space-evenly;
            .item-container {
                height: 120px;
                justify-content: center;
                padding: 0 1rem;
                img {
                    height: 40%;
                    width: 50px;
                    object-fit: contain;
                }
                span {
                    color: white;
                    text-transform: uppercase;
                    text-align: center;
                    padding-left: 0.5rem;
                    font-size: 0.9rem;
                }
            }
        }
    }

    h1 {
        padding: 3rem 0;
        color: white;
    }
}
</style>
