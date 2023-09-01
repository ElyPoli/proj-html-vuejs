<script>
export default {
}
</script>

<template>
    <div class="container tabs-container">
        <div class="row gy-3">
            <div class="col-12 col-sm-3">
                <div class="tabs-navigation">
                    <ul class="list-group">
                        <li class="list-group-item">What We Do</li>
                        <li class="list-group-item">Degree Programme</li>
                        <li class="list-group-item">Career Achievements</li>
                        <li class="list-group-item">Personal Managment</li>
                        <li class="list-group-item">Steps To Success</li>
                        <li class="list-group-item">Knowledge Transfer</li>
                    </ul>
                </div>
            </div>
            <div class="col-12 col-sm-9 d-flex align-items-center">
                <div class="tabs-card">
                    <h5 class="pb-3">Learning Possibilities</h5>
                    <p class="pb-3">
                        Lorem ipsum gravida nibh vel velit auctor aliquetn sollicitudirem quibibendum auci elit cons
                        equat
                        ipsutis sem nibh id elit. Duis sed odio sit amet nibh vulputate cursus a sit amet mauris. Morbi
                        accumsan ipsum velit. Nam nec tellus a odio tincidunt
                    </p>
                    <div class="row align-items-end">
                        <div class="col-8">
                            <ul class="list-unlisted p-0">
                                <li class="list-group-item">
                                    <i class="fa-solid fa-check pe-1"></i>
                                    We enrich lives through learning.
                                </li>
                                <li class="list-group-item">
                                    <i class="fa-solid fa-check pe-1"></i>
                                    Maximizing potential through individual attention.
                                </li>
                                <li class="list-group-item">
                                    <i class="fa-solid fa-check pe-1"></i>
                                    The trusted name for specialized training.
                                </li>
                                <li class="list-group-item">
                                    <i class="fa-solid fa-check pe-1"></i>
                                    People teach. People learn. This is where they connect.
                                </li>
                            </ul>
                        </div>
                        <div class="col-4">
                            <img src="/public/img/tabs-icon-1.png" alt="What We Do">
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<style lang="scss" scoped>
@use "../styles/partials/variables" as *;

.tabs-container {
    padding-top: 8rem;
}

.tabs-navigation {
    .list-group {
        --bs-list-group-item-padding-x: 1rem;
        --bs-list-group-item-padding-y: 1.5rem;
        border-radius: 0;
        font-family: Merriweather, serif;
    }

    .list-group-item {
        color: $light-grey;
        background-color: #ffffff;
        border: var(--bs-list-group-border-width) solid $background-light;
        cursor: pointer;
        transition: all .3s;

        &:hover {
            border-left: 7px solid $primary-color;
            color: $primary-color;
        }
    }
}

.tabs-card {
    padding-left: 4rem;
    padding-right: 4rem;

    img {
        width: 150px;
    }

    h5 {
        font-size: $section-title-size;
    }

    p {
        color: $light-grey;
    }

    li {
        color: $light-grey;
        padding-top: 1rem;

        i {
            color: $primary-color;
        }
    }
}
</style>