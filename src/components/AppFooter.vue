<template>
    <footer>
        <div class="container d-flex">
            <div class="list-container">
                <h2>Dc Comics</h2>
                <ul>
                    <li v-for="element in comicList">
                        <a href="#">{{ element.name }}</a>
                    </li>
                </ul>
                <h2>Shop</h2>
                <ul>
                    <li v-for="element in shopList">
                        <a href="#">{{ element.name }}</a>
                    </li>
                </ul>
            </div>
            <div class="list-container">
                <h2>DC</h2>
                <ul>
                    <li v-for="element in DClist">
                        <a href="#">{{ element.name }}</a>
                    </li>
                </ul>
            </div>
            <div class="list-container">
                <h2>Sites</h2>
                <ul>
                    <li v-for="element in sitesList">
                        <a href="#">{{ element.name }}</a>
                    </li>
                </ul>
            </div>
        </div>
        <div class="w-100 extended-wrapper">
            <div class="container d-flex">
                <div class="container-button">
                    <button><a href="#">Sign-up now!</a></button>
                </div>
                <div class="media-list">
                    <ul class="d-flex">
                        <li class="d-flex align-center">
                            <span>Follow us</span>
                        </li>
                        <li
                            v-for="img in footerIconsList"
                            class="d-flex align-center">
                            <img :src="getImagePath(img.name)" alt="" />
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
    methods: {
        getImagePath: function (img) {
            return new URL(
                `../assets/vue-dc-comics-1/img/${img}`,
                import.meta.url
            ).href;
        },
    },
    data() {
        return {
            comicList: [
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
            shopList: [
                {
                    name: "Shop DC",
                },
                {
                    name: "Shop DC Collectibles",
                },
            ],
            sitesList: [
                {
                    name: "DC",
                },
                {
                    name: "MAD Magazines",
                },
                {
                    name: "DC Kids",
                },
                {
                    name: "DC Universe",
                },
                {
                    name: "DC Power Visa",
                },
            ],
            footerIconsList: [
                {
                    name: "footer-facebook.png",
                },
                {
                    name: "footer-periscope.png",
                },
                {
                    name: "footer-pinterest.png",
                },
                {
                    name: "footer-twitter.png",
                },
                {
                    name: "footer-youtube.png",
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
        top: -45px;
        right: 5%;
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

            a {
                color: rgb(180, 180, 180);
                text-decoration: none;
                &:hover {
                    color: white;
                    text-decoration: underline;
                    cursor: pointer;
                }
            }
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
            position: relative;
            z-index: 1;
            button {
                background-color: transparent;
                color: white;
                border: 1px solid $primaryColor;
                text-transform: uppercase;
                padding: 0.5rem 0.5rem;
                font-size: 1.2rem;
            }
            li {
                margin: 0 0.6rem;
                text-transform: uppercase;
                color: $primaryColor;
                img {
                    width: 70%;
                    transition: scale 0.2s ease-out;
                    &:hover {
                        filter: invert(1);
                        scale: 1.3;
                    }
                }
            }
        }
    }
}
</style>
