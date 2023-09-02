<script>
export default {
}
</script>

<template>
    <div class="container pt-5 pb-5">
        <div class="text-center pt-2 pb-5">
            <h4 class="pb-3">The Best Tutors in Town</h4>
            <p>
                Lorem ipsum gravida nibh vel velit auctor aliquetnean sollicitudin, lorem quis bibendum auci elit consequat
                ipsutis sem nibh id elit
            </p>
        </div>
        <div class="row row-cols-1 row-cols-md-3 gy-2 gx-5">
            <!-- Card 1 -->
            <div class="col">
                <div class="teacher-box text-center">
                    <img src="/public/img/teacher-img-1.jpg" alt="Brenda Harris">
                    <h5 class="">Brenda Harris</h5>
                    <p class="my-card-subtitle text-uppercase">Teacher</p>
                    <p class="">
                        Lorem ipsum oin gravida nibh vel veliauctor aliquenean sollicitudin, lorem quis bibendum auctor,
                        nisi elit consequa
                    </p>
                    <div class="teacher-social-icons d-flex align-items-center justify-content-center">
                        <i class="fa-brands fa-twitter pe-3"></i>
                        <i class="fa-brands fa-instagram pe-3"></i>
                        <i class="fa-brands fa-facebook-f"></i>
                    </div>
                </div>
            </div>
            <!-- Card 2 -->
            <div class="col">
                <div class="teacher-box text-center">
                    <img src="/public/img/teacher-img-2.jpg" alt="Lisa Griffin">
                    <h5 class="">Lisa Griffin</h5>
                    <p class="my-card-subtitle text-uppercase">Teacher</p>
                    <p class="">
                        Lorem ipsum oin gravida nibh vel veliauctor aliquenean sollicitudin, lorem quis bibendum auctor,
                        nisi elit consequa
                    </p>
                    <div class="teacher-social-icons d-flex align-items-center justify-content-center">
                        <i class="fa-brands fa-twitter pe-3"></i>
                        <i class="fa-brands fa-instagram pe-3"></i>
                        <i class="fa-brands fa-facebook-f"></i>
                    </div>
                </div>
            </div>
            <!-- Card 3 -->
            <div class="col">
                <div class="teacher-box text-center">
                    <img src="/public/img/teacher-img-3.jpg" alt="Victor Green">
                    <h5 class="">Victor Green</h5>
                    <p class="my-card-subtitle text-uppercase">Teacher</p>
                    <p class="">
                        Lorem ipsum oin gravida nibh vel veliauctor aliquenean sollicitudin, lorem quis bibendum auctor,
                        nisi elit consequa
                    </p>
                    <div class="teacher-social-icons d-flex align-items-center justify-content-center">
                        <i class="fa-brands fa-twitter pe-3"></i>
                        <i class="fa-brands fa-instagram pe-3"></i>
                        <i class="fa-brands fa-facebook-f"></i>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<style lang="scss" scoped>
@use "../styles/partials/variables" as *;

h4 {
    font-size: $section-title-size;
}

.teacher-box {
    p {
        color: $light-grey;
        padding-bottom: .5rem;
    }

    img {
        width: 150px;
        padding-bottom: 2rem;
    }
}

.teacher-social-icons {
    i {
        cursor: pointer;
        color: $light-grey;
        transition: all .2s;

        &:hover {
            color: $primary-color;
        }
    }
}
</style>