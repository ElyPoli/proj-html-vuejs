<script>
export default {
}
</script>

<template>
    <div class="courses-slider-box pt-3 pb-3">
        <div class="container pt-5 pb-5">
            <h4 class="pb-3">Popular Online Courses</h4>
            <p class="pb-4">
                Lorem ipsum dolor sit amet consectetur, adipisicing elit. Vitae fuga tempore maxime. Sed, laborum, quam
                voluptate expedita minus, nulla temporibus dolores nobis excepturi recusandae saepe? Quis sit error iusto!
                Ullam!
            </p>
            <div class="row row-cols-1 row-cols-md-3 justify-content-center">
                <!-- Card 1 -->
                <div class="col">
                    <div class="card">
                        <div class="position-relative">
                            <i class="fa-regular fa-heart"></i>
                            <img src="/public/img/courses-carousel-1.jpg" class="card-img-top" alt="Business English">
                        </div>
                        <div class="card-body">
                            <div class="d-flex align-items-start justify-content-between">
                                <h5 class="card-title">Business English</h5>
                                <span class="badge rounded-pill my-badge my-badge-blue">$20</span>
                            </div>
                            <p class="my-card-subtitle">Preston Marshall</p>
                            <p class="card-text">
                                Lorem ipsum dolor sit, amet consectetur adipisicing elit. Eveniet a voluptatem dolore
                                consequatur.
                            </p>
                            <div class="my-card-tags">
                                <div class="d-flex pe-4">
                                    <i class="fa-solid fa-user"></i>
                                    <p class="my-card-subtitle ps-2">0</p>
                                </div>
                                <div class="d-flex">
                                    <i class="fa-solid fa-tag fa-flip-horizontal"></i>
                                    <p class="my-card-subtitle text-uppercase ps-2">Languages</p>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>
                <!-- Card 2 -->
                <div class="col">
                    <div class="card">
                        <div class="position-relative">
                            <i class="fa-regular fa-heart"></i>
                            <img src="/public/img/courses-carousel-2.jpg" class="card-img-top" alt="Social Computing">
                        </div>
                        <div class="card-body">
                            <div class="d-flex align-items-start justify-content-between">
                                <h5 class="card-title">Social Computing</h5>
                                <span class="badge rounded-pill my-badge my-badge-yellow">FREE</span>
                            </div>
                            <p class="my-card-subtitle">David Sanders</p>
                            <p class="card-text">
                                Lorem ipsum dolor sit, amet consectetur adipisicing elit. Eveniet a voluptatem dolore
                                consequatur.
                            </p>
                            <div class="my-card-tags">
                                <div class="d-flex pe-4">
                                    <i class="fa-solid fa-user"></i>
                                    <p class="my-card-subtitle ps-2">0</p>
                                </div>
                                <div class="d-flex">
                                    <i class="fa-solid fa-tag fa-flip-horizontal"></i>
                                    <p class="my-card-subtitle text-uppercase ps-2">Programming</p>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>
                <!-- Card 3 -->
                <div class="col">
                    <div class="card">
                        <div class="position-relative">
                            <i class="fa-regular fa-heart"></i>
                            <img src="/public/img/courses-carousel-3.jpg" class="card-img-top" alt="Learn Spanish">
                        </div>
                        <div class="card-body">
                            <div class="d-flex align-items-start justify-content-between">
                                <h5 class="card-title">Learn Spanish</h5>
                                <span class="badge rounded-pill my-badge my-badge-blue">$20</span>
                            </div>
                            <p class="my-card-subtitle">Jennie King</p>
                            <p class="card-text">
                                Lorem ipsum dolor sit, amet consectetur adipisicing elit. Eveniet a voluptatem dolore
                                consequatur.
                            </p>
                            <div class="my-card-tags">
                                <div class="d-flex pe-4">
                                    <i class="fa-solid fa-user"></i>
                                    <p class="my-card-subtitle ps-2">0</p>
                                </div>
                                <div class="d-flex">
                                    <i class="fa-solid fa-tag fa-flip-horizontal"></i>
                                    <p class="my-card-subtitle text-uppercase ps-2">Languages</p>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
            <div class="courses-slider-player pt-5">
                <i class="fa-solid fa-circle pe-2"></i>
                <i class="fa-solid fa-circle pe-2"></i>
                <i class="fa-solid fa-circle"></i>
            </div>
        </div>
    </div>
</template>

<style lang="scss" scoped>
@use "../styles/partials/variables" as *;

.courses-slider-box {
    background-image: url("/public/img/section-bg.jpg");
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

        &:first-of-type {
            opacity: 1;
        }
    }
}

.my-badge {
    padding-left: 1rem;
    padding-right: 1rem;
}
.my-badge-blue {
    background-color: $primary-color;
}
.my-badge-yellow {
    background-color: $yellow;
}

</style>