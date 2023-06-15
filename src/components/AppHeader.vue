<template>
    <header>
        <div class="container">
            <nav class="d-flex">
                <div class="img-container d-flex">
                    <img
                        src="../assets/vue-dc-comics-1/img/dc-logo.png"
                        alt="" />
                </div>
                <div class="list-container d-flex h-100">
                    <ul class="d-flex h-100">
                        <li
                            v-for="(link, index) in links"
                            class="d-flex align-center"
                            @click="active(index)"
                            :class="activeIndex === index ? 'active' : ''">
                            <a
                                href="#"
                                :class="activeIndex === index ? 'active' : ''"
                                >{{ link.name }}</a
                            >
                        </li>
                    </ul>
                </div>
            </nav>
        </div>
    </header>
</template>

<script>
export default {
    methods: {
        active(index) {
            this.activeIndex = index;
        },
    },
    data() {
        return {
            activeIndex: 0,
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
        };
    },
};
</script>

<style lang="scss" scoped>
@use "../styles/partials/variables.scss" as *;
header {
    background-color: white;
}
nav {
    justify-content: space-between;
    align-items: center;
    height: 103px;
    .img-container {
        height: 100%;
        align-items: center;
        img {
            height: 80%;
            display: block;
        }
    }
    .list-container {
        align-items: center;
        ul {
            li {
                margin: 0.5rem 0.75rem;
                text-transform: uppercase;
                margin: 0;
                margin-left: 1rem;
                position: relative;
                a.active {
                    color: $primaryColor;
                }
                &.active::after {
                    content: "";
                    position: absolute;
                    bottom: 0;
                    top: 93%;
                    left: 0;
                    right: 0;
                    background-color: $primaryColor;
                }
                a {
                    color: black;
                    text-decoration: none;
                    &:hover {
                        color: $primaryColor;
                    }
                }
            }
        }
    }
}
</style>
