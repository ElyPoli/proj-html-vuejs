<script>
export default {
    data() {
        return {
            cardMenu: [
                {
                    name: "Languages",
                    img: "card-menu-1.png",
                },
                {
                    name: "Software",
                    img: "card-menu-2.png",
                },
                {
                    name: "Business",
                    img: "card-menu-3.png",
                },
                {
                    name: "Chemistry",
                    img: "card-menu-4.png",
                },
                {
                    name: "Science",
                    img: "card-menu-5.png",
                },
                {
                    name: "DIY&Craft",
                    img: "card-menu-6.png",
                },
            ]
        }
    }
}
</script>

<template>
    <div class="container pt-2 pb-5">
        <div class="row row-cols-lg-6 row-cols-md-3 row-cols-sm-2 row-cols-1 gy-3">
            <div class="col" v-for="(card, i) in cardMenu" :key="i">
                <div class="my-card-menu">
                    <div>
                        <img v-bind:src="`/public/img/${card.img}`" v-bind:alt="card.name">
                        <h5>{{ card.name }}</h5>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<style lang="scss" scoped>
@use "../styles/partials/variables" as *;

.my-card-menu {
    background-color: $background-light;
    height: 200px;
    width: 100%;
    display: flex;
    align-items: center;
    justify-content: center;
    cursor: pointer;

    h5 {
        margin: 0;
        padding-top: 1.5rem;
        font-weight: bold;
        font-size: 1rem;
    }

    img {
        transition: transform .5s;
    }

    &:hover img {
        transform: translateY(-8%);
    }
}
</style>