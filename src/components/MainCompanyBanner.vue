<script>
export default {
    data() {
        return {
            companysList: [
                {
                    name: "StudyCentral",
                    img: "company-logo-1.png",
                },
                {
                    name: "Educator",
                    img: "company-logo-2.png",
                },
                {
                    name: "TeachHub",
                    img: "company-logo-3.png",
                },
                {
                    name: "Scholar",
                    img: "company-logo-4.png",
                },
                {
                    name: "iAcademy",
                    img: "company-logo-5.png",
                },
            ]
        }
    }
}
</script>

<template>
    <div class="container pt-5 pb-5">
        <div class="row row-cols-lg-5 row-cols-md-3 row-cols-sm-2 row-cols-1 gy-4">
            <div class="col" v-for="(card, i) in companysList" :key="i">
                <div class="company-banner-box">
                    <div>
                        <img v-bind:src="`/public/img/${card.img}`" v-bind:alt="card.name">
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<style lang="scss" scoped>
@use "../styles/partials/variables" as *;

.company-banner-box {
    cursor: pointer;
    display: flex;
    justify-content: center;

    img {
        transition: opacity .5s;
    }

    &:hover img {
        opacity: .7;
    }
}
</style>