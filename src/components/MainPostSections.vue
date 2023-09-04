<script>
export default {
}
</script>

<template>
    <!-- Sezione 1 -->
    <div class="container pt-2">
        <div class="row row-cols-1 row-cols-lg-2 align-items-center gy-2">
            <div class="col my-section-box">
                <h3 class="pe-5">The Trusted Name for In-Home Tutoring.</h3>
                <p class="pe-5">
                    Lorem ipsum gravida nibh vel velit auctor aliquetnean sollicitudin, lorem quis bibendum auci elit
                    consequat ipsutis sem nibh id eis sed odio sit amet nibh vulputate cursus mauris.
                </p>
                <div class="my-section-link">
                    <a href="#">Learn More</a>
                    <i class="fa-solid fa-chevron-right"></i>
                </div>
            </div>
            <div class="col my-section-box">
                <img src="/public/img/section1-img.jpg" alt="In-Home Tutoring">
            </div>
        </div>
    </div>

    <!-- Linea divisoria -->
    <div class="my-section-line"></div>

    <!-- Sezione 2 -->
    <div class="container pt-5">
        <div class="row row-cols-1 row-cols-lg-2 align-items-center gy-2">
            <!-- Sezione 2 -->
            <div class="col my-section-box">
                <img src="/public/img/section2-img.jpg" alt="Empowering Children">
            </div>
            <div class="col my-section-box">
                <h3 class="ps-5">Empowering Children to Reach Their Potential.</h3>
                <p class="ps-5">
                    Lorem ipsum gravida nibh vel velit auctor aliquetnean sollicitudin, lorem quis bibendum auci elit
                    consequat ipsutis sem nibh id eis sed odio sit amet nibh vulputate.
                </p>
                <div class="my-section-counter ps-5">
                    <div class="pe-5">
                        <h4>168</h4>
                        <h5>User Stories</h5>
                    </div>
                    <div class="ps-5">
                        <h4>347</h4>
                        <h5>Events</h5>
                    </div>
                </div>
            </div>
        </div>
    </div>

    <!-- Immagine divisoria -->
    <div class="divider-img">
        <img src="/public/img/section-bg.jpg" alt="bg image">
    </div>
</template>

<style lang="scss" scoped>
@use "../styles/partials/variables" as *;

.my-section-box {
    overflow: hidden;

    img {
        height: 500px;
        width: 650px;
        object-fit: cover;
        margin-right: 2rem;
    }

    h3 {
        font-size: $section-title-size;
        padding-bottom: 1rem;
        margin: 0;
    }

    p {
        margin: 0;
        padding-bottom: 2rem;
        line-height: 1.7rem;
        font-size: 1.2rem;
        color: $light-grey;
    }
}

.my-section-link {
    a {
        text-transform: uppercase;
        color: $primary-color;
        position: relative;

        &:hover {
            +i {
                opacity: 1;
                padding-left: .3rem;
            }
        }
    }

    i {
        opacity: 0;
        color: $primary-color;
        transition: all .3s;
    }
}

.my-section-line {
    border-bottom: 1px solid $background-light;
}

.my-section-counter {
    display: flex;
    align-items: center;
    justify-content: start;

    h4,
    h5 {
        color: $primary-color;
    }

    h4 {
        font-size: $section-title-size;
    }

}

.divider-img {
    overflow: hidden;
    height: 150px;

    img {
        object-fit: contain;
    }
}
</style>