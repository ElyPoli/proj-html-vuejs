<script>
export default {
}
</script>

<template>
    <div class="testimonials-container d-flex text-center justify-content-center align-items-center">
        <div class="container w-50">
            <img src="/public/img/testimonials-img-1.png" alt="testimonial">
            <p class="pb-2 pt-4">
                “Mroin gravida nibh vel veliauctor aliquenean sollicitudin, lorem quis bibendum auctor, nisi elit
                consequat
                ipsutis sem nibh id elit. Duis sed odio sit amet nivulputate cursus a sit amet mauris. Morbi accumsan
                ipsum
                velit. Nam nec tellus”
            </p>
            <h5 class="m-0 pt-2 pb-2">Molly Simon</h5>
            <p class="m-0 pt-2 pb-2 text-uppercase fw-bold">Teacher</p>
            <div class="pt-3">
                <i class="fa-solid fa-circle pe-2"></i>
                <i class="fa-solid fa-circle pe-2"></i>
                <i class="fa-solid fa-circle"></i>
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

        &:first-of-type {
            opacity: 1;
        }
    }
}
</style>