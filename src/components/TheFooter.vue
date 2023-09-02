<script>
export default {
    data() {
        return {
            footerNav: [
                {
                    title: "",
                    name: "iAcademy",
                    logo: "logo-light.png",
                    imgBg: "",
                    desc: "Providing Life Changing Experiences Through Education. Class That Fit Your Busy Life. Closer to Home",
                    linkList: "",
                    celNum: "1-677-124-44227",
                    hourNum: "Mon - Sat 8.00 - 18.00",
                },
                {
                    title: "Popular Courses",
                    name: "",
                    logo: "",
                    imgBg: "",
                    desc: "",
                    linkList: [
                        { title: "Business English", subheading: "Preston Marshall", text: "" },
                        { title: "Social computing", subheading: "David Sanders", text: "" },
                        { title: "Learn Spanish", subheading: "Jennie King", text: "" },
                    ],
                    celNum: "",
                    hourNum: "",
                },
                {
                    title: "Support",
                    name: "",
                    logo: "",
                    imgBg: "",
                    desc: "",
                    linkList: [
                        { title: "", subheading: "", text: "User dashboard" },
                        { title: "", subheading: "", text: "Contact Us" },
                        { title: "", subheading: "", text: "FAQ" },
                        { title: "", subheading: "", text: "Course Offer" },
                        { title: "", subheading: "", text: "Events" },
                    ],
                    celNum: "",
                    hourNum: "",
                },
                {
                    title: "Flexible Learning",
                    name: "Flexible Learning Map",
                    logo: "",
                    imgBg: "footer-map.png",
                    desc: "",
                    linkList: "",
                    celNum: "",
                    hourNum: "",
                },
            ]
        }
    }
}
</script>

<template>
    <footer>
        <div class="container">
            <!-- Parte superiore -->
            <div class="my-footer-top">
                <div class="row row-cols-1 row-cols-sm-2 row-cols-lg-4">
                    <div class="col" v-for="(element, i) in footerNav" :key="i">
                        <h6 class="pb-4" v-if="element.title">{{ element.title }}</h6>
                        <img class="footer-logo pb-4" v-bind:src="`/public/img/${element.logo}`" v-bind:alt="element.name"
                            v-if="element.logo">
                        <p v-if="element.desc"> {{ element.desc }} </p>
                        <ul class="list-unstyled" v-if="element.linkList" v-for="(link, z) in element.linkList" :key="z">
                            <li>
                                <a class="fw-bold" href="#" v-if="link.title"> {{ link.title }} </a>
                                <p class="link-subheading" v-if="link.subheading"> {{ link.subheading }} </p>
                                <p class="link-text" v-if="link.text"> {{ link.text }} </p>
                            </li>
                        </ul>
                        <img class="footer-map" v-bind:src="`/public/img/${element.imgBg}`" v-bind:alt="element.name"
                            v-if="element.imgBg">
                        <div>
                            <span class="icon-link pb-2" v-if="element.celNum"><i class="fa-solid fa-phone pe-2"></i> {{ element.celNum }}</span>
                            <span class="icon-link" v-if="element.hourNum"><i class="fa-solid fa-clock pe-2"></i> {{ element.hourNum }}</span>
                        </div>
                    </div>
                </div>
            </div>
            <!-- Parte inferiore -->
            <div class="my-footer-bottom">
                <p class="">© 2017 Qode Interactive, All Rights Reserved</p>
                <div class="d-flex">
                    <p>CALL +44 300 303 0266</p>
                    <p class="text-uppercase ps-3">Follow Us</p>
                </div>
            </div>
        </div>
    </footer>
</template>

<style lang="scss" scoped>
@use "../styles/partials/variables" as *;

footer {
    background-color: $dark-grey;
    padding-top: 4rem;
    padding-bottom: 2rem;

    h6 {
        color: #ffffff;
        font-size: 1.2rem;
    }

    p,
    li {
        color: $light-grey;
    }
}

.my-footer-top {
    padding-bottom: 3rem;

    .footer-logo {
        width: 150px;
        cursor: pointer;
    }

    .footer-map {
        width: 300px;
        cursor: pointer;
    }

    a {
        color: $light-grey;

        &:hover,
        &:active,
        &:focus {
            color: $primary-color;
        }
    }

    .link-subheading {
        font-size: .9rem;
        cursor: pointer;
        font-weight: bold;

        &:hover {
            color: $grey;
        }
    }

    .link-text {
        cursor: pointer;

        &:hover {
            color: $primary-color;
        }
    }

    .icon-link {
        cursor: pointer;
        color: $light-grey;

        &:hover {
            i {
                color: $primary-color;
            }
        }
    }
}

.my-footer-bottom {
    display: flex;
    align-items: center;
    justify-content: space-between;
    font-size: .8rem;
    border-top: 1px solid $grey;
    padding-top: 2rem;

    >p {
        cursor: pointer;
    }
}</style>