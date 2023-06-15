<template>
    <main>
        <div class="extended-wrapper bg-black">
            <div class="container">
                <h1>--> Content goes here &lt;--</h1>
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
export default {
    data() {
        return {};
    },
};
</script>

<style lang="scss" scoped>
main {
    .extended-wrapper {
        width: 100%;
        .items {
            justify-content: space-evenly;
            .item-container {
                height: 120px;
                justify-content: center;
                padding: 0 1rem;
                img {
                    height: 60%;
                    width: 70px;
                    object-fit: contain;
                }
                span {
                    color: white;
                    text-transform: uppercase;
                    text-align: center;
                    padding-left: 0.5rem;
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
