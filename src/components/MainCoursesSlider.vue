<script>
export default {
    data() {
        return {
            coursesList: [
                [
                    {
                        title: "Business English",
                        subheading: "Preston Marshall",
                        img: "courses-carousel-1.jpg",
                        text: "Lorem ipsum dolor sit, amet consectetur adipisicing elit. Eveniet a voluptatem dolore consequatur.",
                        type: "Languages",
                        subscribers: "0",
                        pay: "$20",
                        free: "",
                    },
                    {
                        title: "Social Computing",
                        subheading: "David Sanders",
                        img: "courses-carousel-2.jpg",
                        text: "Lorem ipsum dolor sit, amet consectetur adipisicing elit. Eveniet a voluptatem dolore consequatur.",
                        type: "Programming",
                        subscribers: "0",
                        pay: "",
                        free: "Free",
                    },
                    {
                        title: "Learning Spanish",
                        subheading: "Jennie King",
                        img: "courses-carousel-3.jpg",
                        text: "Lorem ipsum dolor sit, amet consectetur adipisicing elit. Eveniet a voluptatem dolore consequatur.",
                        type: "Languages",
                        subscribers: "0",
                        pay: "$20",
                        free: "",
                    },
                ],
                [
                    {
                        title: "Basic Marketing",
                        subheading: "Edward Bowman",
                        img: "courses-carousel-4.jpg",
                        text: "Lorem ipsum dolor sit, amet consectetur adipisicing elit. Eveniet a voluptatem dolore consequatur.",
                        type: "Business",
                        subscribers: "0",
                        pay: "$40",
                        free: "",
                    },
                    {
                        title: "Android Developer",
                        subheading: "David Sanders",
                        img: "courses-carousel-5.jpg",
                        text: "Lorem ipsum dolor sit, amet consectetur adipisicing elit. Eveniet a voluptatem dolore consequatur.",
                        type: "Programming",
                        subscribers: "0",
                        pay: "",
                        free: "Free",
                    },
                    {
                        title: "Web Designing",
                        subheading: "Jennifer Powell",
                        img: "courses-carousel-6.jpg",
                        text: "Lorem ipsum dolor sit, amet consectetur adipisicing elit. Eveniet a voluptatem dolore consequatur.",
                        type: "Programming",
                        subscribers: "0",
                        pay: "",
                        free: "Free",
                    },
                ],
                [
                    {
                        title: "Financial Modeling",
                        subheading: "Edward Bowman",
                        img: "courses-carousel-7.jpg",
                        text: "Lorem ipsum dolor sit, amet consectetur adipisicing elit. Eveniet a voluptatem dolore consequatur.",
                        type: "Business",
                        subscribers: "0",
                        pay: "$20",
                        free: "",
                    },
                    {
                        title: "Academic English",
                        subheading: "Dave Robbins",
                        img: "courses-carousel-8.jpg",
                        text: "Lorem ipsum dolor sit, amet consectetur adipisicing elit. Eveniet a voluptatem dolore consequatur.",
                        type: "Languages",
                        subscribers: "0",
                        pay: "",
                        free: "Free",
                    },
                    {
                        title: "Modern Psychology",
                        subheading: "Kathryn Webb",
                        img: "courses-carousel-9.jpg",
                        text: "Lorem ipsum dolor sit, amet consectetur adipisicing elit. Eveniet a voluptatem dolore consequatur.",
                        type: "Business",
                        subscribers: "0",
                        pay: "$40",
                        free: "",
                    },
                ],
            ],
            currentSlide: 0,
        }
    },
    methods: {
        btnChangeSlide(index) {
            this.currentSlide = index;
        }
    },
}
</script>

<template>
    <div class="courses-slider-box geometric-bg pt-3 pb-3">
        <div class="container pt-5 pb-5">
            <h4 class="pb-3">Popular Online Courses</h4>
            <p class="pb-4">
                Lorem ipsum dolor sit amet consectetur, adipisicing elit. Vitae fuga tempore maxime. Sed, laborum, quam
                voluptate expedita minus, nulla temporibus dolores nobis excepturi recusandae saepe? Quis sit error iusto!
                Ullam!
            </p>
            <div class="row row-cols-1 row-cols-md-3 justify-content-center" v-for="(cardGroup, i) in coursesList" :key="i">
                <!-- Card  -->
                <div v-for="(card, z) in cardGroup" :key="z"
                    v-bind:class="(currentSlide === i ? 'col courses-active courses-card' : 'col courses-card')">
                    <div class="card">
                        <div class="position-relative">
                            <i class="fa-regular fa-heart"></i>
                            <img v-bind:src="`/public/img/${card.img}`" class="card-img-top" v-bind:alt="card.title">
                        </div>
                        <div class="card-body">
                            <div class="d-flex align-items-start justify-content-between">
                                <h5 class="card-title">{{ card.title }}</h5>
                                <span class="badge rounded-pill my-badge my-badge-blue" v-if="card.pay">
                                    {{ card.pay }}
                                </span>
                                <span class="badge rounded-pill my-badge my-badge-yellow text-uppercase" v-if="card.free">
                                    {{ card.free }}
                                </span>
                            </div>
                            <p class="my-card-subtitle">{{ card.subheading }}</p>
                            <p class="card-text">{{ card.text }}</p>
                            <div class="my-card-tags">
                                <div class="d-flex pe-4">
                                    <i class="fa-solid fa-user"></i>
                                    <p class="my-card-subtitle ps-2">{{ card.subscribers }}</p>
                                </div>
                                <div class="d-flex">
                                    <i class="fa-solid fa-tag fa-flip-horizontal"></i>
                                    <p class="my-card-subtitle text-uppercase ps-2">{{ card.type }}</p>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
            <!-- Pulsanti di navigazione -->
            <div class="courses-slider-player pt-5">
                <i v-for="(btn, i) in coursesList" :key="i" @click="btnChangeSlide(i)"
                    v-bind:class="(currentSlide === i ? 'fa-solid fa-circle pe-2 courses-btn-active' : 'fa-solid fa-circle pe-2')">
                </i>
            </div>
        </div>
    </div>
</template>

<style lang="scss" scoped>
@use "../styles/partials/variables" as *;

.courses-slider-box {
    text-align: center;
    border-bottom: 1px solid $background-light;
    border-top: 1px solid $background-light;
    margin-top: 5rem;

    h4 {
        font-size: $section-title-size;
    }

    p {
        color: $light-grey;
    }
}

.card {
    border-radius: 0;
    border-color: $background-light;
    text-align: start;
    margin-top: 2.5rem;
    cursor: pointer;
    transition: all .5s;

    img {
        transition: all .5s;
    }

    .fa-heart {
        position: absolute;
        right: 0;
        top: 0;
        color: white;
        padding-top: 1rem;
        padding-right: 1rem;
        opacity: 0;
        z-index: 1;
    }


    &:hover {
        transform: translateY(-2%);
        box-shadow: 2px 2px 10px 0px rgb(0, 0, 0, .1);


        img {
            filter: brightness(.8);
        }

        .fa-heart {
            opacity: 1;
            transition: all .5s;
        }
    }
}

.courses-card {
    display: none;
}

.courses-active.courses-card {
    display: block;
}

.my-card-tags {
    color: $light-grey;
    cursor: pointer;
    display: flex;

    div {
        &:hover {
            color: $grey;
        }
    }
}

.courses-slider-player {
    i {
        color: $primary-color;
        opacity: .5;
        transition: opacity .5s;
        cursor: pointer;
        font-size: .8rem;

        &:hover,
        &:active {
            opacity: 1;
        }
    }

    i.courses-btn-active {
        opacity: 1;
    }
}
</style>