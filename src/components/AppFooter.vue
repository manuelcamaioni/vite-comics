<template>
    <footer>
        <div class="container d-flex">
            <div class="list-container">
                <h2>Dc Comics</h2>
                <ul>
                    <li v-for="link in links">{{ link.name }}</li>
                </ul>
                <h2>Shop</h2>
                <ul>
                    <li>Shop DC</li>
                    <li>Shop DC Collectibles</li>
                </ul>
            </div>
            <div class="list-container">
                <h2>DC</h2>
                <ul>
                    <li v-for="element in DClist">{{ element.name }}</li>
                </ul>
            </div>
            <div class="list-container">
                <h2>Sites</h2>
                <ul>
                    <li>DC</li>
                    <li>MAD Magazines</li>
                    <li>DC Kids</li>
                    <li>DC Universe</li>
                    <li>DC Power Visa</li>
                </ul>
            </div>
        </div>
        <div class="w-100 extended-wrapper">
            <div class="container d-flex">
                <div class="container-button">
                    <button>Sign-up now!</button>
                </div>
                <div class="media-list">
                    <ul class="d-flex">
                        <li class="d-flex align-center">
                            <span>Follow us</span>
                        </li>
                        <li class="d-flex align-center">
                            <img
                                src="../assets/vue-dc-comics-1/img/footer-facebook.png"
                                alt="" />
                        </li>
                        <li class="d-flex align-center">
                            <img
                                src="../assets/vue-dc-comics-1/img/footer-periscope.png"
                                alt="" />
                        </li>
                        <li class="d-flex align-center">
                            <img
                                src="../assets/vue-dc-comics-1/img/footer-pinterest.png"
                                alt="" />
                        </li>
                        <li class="d-flex align-center">
                            <img
                                src="../assets/vue-dc-comics-1/img/footer-twitter.png"
                                alt="" />
                        </li>
                        <li class="d-flex align-center">
                            <img
                                src="../assets/vue-dc-comics-1/img/footer-youtube.png"
                                alt="" />
                        </li>
                    </ul>
                </div>
            </div>
        </div>
        <div class="overlay-container"></div>
    </footer>
</template>

<script>
export default {
    data() {
        return {
            links: [
                {
                    name: "Characters",
                },
                {
                    name: "Comics",
                },
                {
                    name: "Movies",
                },
                {
                    name: "TV",
                },
                {
                    name: "Games",
                },
                {
                    name: "Collectibles",
                },
                {
                    name: "Videos",
                },
                {
                    name: "Fans",
                },
                {
                    name: "News",
                },
                {
                    name: "Shop",
                },
            ],
            DClist: [
                {
                    name: "Terms of Use",
                },
                {
                    name: "Privacy Policy (News)",
                },
                {
                    name: "Ad Choices",
                },
                {
                    name: "Advertising",
                },
                {
                    name: "Jobs",
                },
                {
                    name: "Subscriptions",
                },
                {
                    name: "Talent Workshops",
                },
                {
                    name: "CPSC Certificates",
                },
                {
                    name: "Ratings",
                },
                {
                    name: "Shop Help",
                },
                {
                    name: "Contact us",
                },
            ],
        };
    },
};
</script>

<style lang="scss" scoped>
@use "../styles/partials/variables.scss" as *;
footer {
    background: url("../assets/vue-dc-comics-1/img/footer-bg.jpg") no-repeat;
    background-size: cover;
    position: relative;
    color: white;
    .overlay-container {
        position: absolute;
        top: 0;
        right: 20%;
        width: 700px;
        height: 456px;
        background: url("../assets/vue-dc-comics-1/img/dc-logo-bg.png")
            no-repeat;
    }
    .list-container {
        margin-bottom: 1rem;
        margin-right: 1rem;
        li {
            margin-bottom: 0.2rem;
        }
    }
    h2 {
        padding: 1rem 0;
        text-transform: uppercase;
    }

    .extended-wrapper {
        background-color: #303030;
        padding: 2rem 0;
        z-index: 1;
        position: relative;
        .container {
            justify-content: space-between;
            align-items: center;
            button {
                background-color: transparent;
                color: white;
                border: 1px solid $primaryColor;
                text-transform: uppercase;
                padding: 0.5rem 0.5rem;
            }
            li {
                margin-left: 0.5rem;
                text-transform: uppercase;
                color: $primaryColor;
                img {
                    width: 70%;
                }
            }
        }
    }
}
</style>
