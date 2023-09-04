<script>
export default {
    data() {
        return {
            testimonialsList: [
                {
                    name: "Molly Simon",
                    text: `“Mroin gravida nibh vel veliauctor aliquenean sollicitudin, lorem quis bibendum auctor, nisi elit consequat ipsutis sem nibh id elit. Duis sed odio sit amet nivulputate cursus a sit amet mauris. Morbi accumsan ipsum velit. Nam nec tellus”`,
                    occupation: "Teacher",
                    img: "testimonials-img-1.png",
                },
                {
                    name: "Joan Collins",
                    text: `“Mroin gravida nibh vel veliauctor aliquenean sollicitudin, lorem quis bibendum auctor, nisi elit consequat ipsutis sem nibh id elit. Duis sed odio sit amet nivulputate cursus a sit amet mauris. Morbi accumsan ipsum velit. Nam nec tellus”`,
                    occupation: "Student",
                    img: "testimonials-img-2.png",
                },
                {
                    name: "Virginia Foster",
                    text: `“Mroin gravida nibh vel veliauctor aliquenean sollicitudin, lorem quis bibendum auctor, nisi elit consequat ipsutis sem nibh id elit. Duis sed odio sit amet nivulputate cursus a sit amet mauris. Morbi accumsan ipsum velit. Nam nec tellus”`,
                    occupation: "Student",
                    img: "testimonials-img-3.png",
                },
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
    <div class="testimonials-container d-flex text-center justify-content-center align-items-center">
        <div class="container w-50">
            <div v-for="(testimonial, i) in testimonialsList" :key="i"
                v-bind:class="(currentSlide === i ? 'testimonials-active testimonials-card' : 'testimonials-card')">
                <img v-bind:src="`/public/img/${testimonial.img}`" v-bind:alt="testimonial.name">
                <p class="pb-2 pt-4">{{ testimonial.text }}</p>
                <h5 class="m-0 pt-2 pb-2">{{ testimonial.name }}</h5>
                <p class="m-0 pt-2 pb-2 text-uppercase fw-bold">{{ testimonial.occupation }}</p>
            </div>
            <div class="pt-3">
                <i v-for="(testimonial, i) in testimonialsList" :key="i" @click="btnChangeSlide(i)"
                    v-bind:class="(currentSlide === i ? 'fa-solid fa-circle pe-2 testimonials-btn-active' : 'fa-solid fa-circle pe-2')">
                </i>
            </div>
        </div>
    </div>
</template>

<style lang="scss" scoped>
@use "../styles/partials/variables" as *;

.testimonials-container {
    background-image: url("/public/img/testimonials-background.png");
    height: 550px;

    p,
    h5,
    h6,
    i {
        color: white;
    }

    i {
        opacity: .5;
        transition: opacity .5s;
        cursor: pointer;
        font-size: .8rem;

        &:hover,
        &:active {
            opacity: 1;
        }
    }

    i.testimonials-btn-active {
        opacity: 1;
    }

    .testimonials-card {
        display: none;
        opacity: 0;
        transition: opacity .5s;
    }

    .testimonials-card.testimonials-active {
        display: inline-block;
        opacity: 1;
    }
}
</style>