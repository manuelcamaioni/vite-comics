<template>
    <header>
        <div class="container">
            <nav class="d-flex">
                <div class="img-container">
                    <img
                        src="../assets/vue-dc-comics-1/img/dc-logo.png"
                        alt="" />
                </div>
                <div class="list-container d-flex">
                    <ul class="d-flex">
                        <li v-for="link in links">{{ link.name }}</li>
                    </ul>
                </div>
            </nav>
        </div>
    </header>
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
        };
    },
};
</script>

<style lang="scss" scoped>
header {
    background-color: white;
}
nav {
    justify-content: space-between;
    .list-container {
        align-items: center;
        ul {
            li {
                margin: 0.5rem 0.75rem;
                text-transform: uppercase;
            }
        }
    }
}
</style>
