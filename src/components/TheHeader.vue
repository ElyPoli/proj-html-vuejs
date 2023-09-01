<script>
export default {
    data() {
        return {
            homeLinks: [
                { name: "Home 1", star: false, active: false },
                { name: "Home 2", star: true, active: false },
                { name: "Home 3", star: false, active: false },
                { name: "Home 4", star: true, active: false },
                { name: "Home 5", star: false, active: false },
                { name: "Home 6", star: false, active: false },
                { name: "Home 7", star: false, active: false },
                { name: "Home 8", star: false, active: false },
                { name: "Home 9", star: false, active: false },
                { name: "Home 10", star: true, active: true },
                { name: "Home 11", star: false, active: false },
                { name: "Home 12", star: true, active: false },
                { name: "Landing", star: false, active: false },
            ],
            coursesLinks: [
                {
                    subtitle: "Features",
                    childsLink: [
                        { name: "All Courses", img: "" },
                        { name: "Standard List", img: "" },
                        { name: "Course Single", img: "" },
                        { name: "User dashboard", img: "" },
                    ]
                },
                {
                    subtitle: "Business",
                    childsLink: [
                        { name: "", img: "courses-carousel-4.jpg", cost: "$40", pay: "true" },
                    ]
                },
                {
                    subtitle: "Languages",
                    childsLink: [
                        { name: "", img: "courses-carousel-1.jpg", cost: "$20", pay: "true" },
                    ]
                }
                ,
                {
                    subtitle: "Programming",
                    childsLink: [
                        { name: "", img: "courses-carousel-2.jpg", cost: "FREE", pay: "false" },
                    ]
                },
            ],
            instructorsLinks: [
                { name: "Become an Instructor" },
                { name: "Instructor Single" },
            ],
            eventsLinks: [
                { name: "Events Calendar" },
                { name: "Events List" },
                { name: "Event Single" },
            ],
            pagesLinks: [
                { name: "About" },
                { name: "Gallery" },
                { name: "Pricing Plan" },
                { name: "Blog", },
                { name: "Shop", },
                { name: "Forums", },
                { name: "Contact" },
                { name: "FAQ" },
                { name: "Coming Soon" },
                { name: "Error Page" },
            ],
            elementsLinks: [
                {
                    subtitle: "Course Shortcodes",
                    childsLink: [
                        { name: "Course List" },
                        { name: "Course Slider" },
                        { name: "Course Table" },
                        { name: "Course Features" },
                        { name: "Instructor List" },
                        { name: "Instructor Slider" },
                        { name: "Education Timeline" },
                        { name: "Advanced Course Search" },
                        { name: "Link Image List" },
                    ]
                },
                {
                    subtitle: "Classic",
                    childsLink: [
                        { name: "Accordions & Toggles" },
                        { name: "Tabs" },
                        { name: "Buttons" },
                        { name: "Call To Action" },
                        { name: "Contact Form" },
                        { name: "Separators" },
                        { name: "Icon Width Text" },
                        { name: "Blockquote" },
                        { name: "Typography" },
                    ]
                },
                {
                    subtitle: "Course Shortcodes",
                    childsLink: [
                        { name: "Couunters" },
                        { name: "Countdown" },
                        { name: "Pie Charts" },
                        { name: "Google Maps" },
                        { name: "Process" },
                        { name: "Progress Bar" },
                        { name: "Events List" },
                        { name: "Pricing Tables" },
                        { name: "Comparison Pricing Tables" },
                    ]
                },
                {
                    subtitle: "Presentation",
                    childsLink: [
                        { name: "Team Shortcode" },
                        { name: "Testimonials" },
                        { name: "Clients" },
                        { name: "Blog List Shortcode" },
                        { name: "Twitter List" },
                        { name: "Product List" },
                        { name: "Image Gallery" },
                        { name: "Masonry Gallery" },
                        { name: "Video Button" },
                    ]
                },
            ],
        };
    },
}
</script>

<template>
    <header>
        <nav class="navbar navbar-expand-lg bg-success pt-3">
            <div class="container d-flex align-items-center justify-content-between">
                <div>
                    <a class="navbar-brand" href="#">
                        <img src="/public/img/logo-light.png" alt="iAcademy">
                    </a>
                </div>
                <div class="d-flex align-items-center">
                    <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarNav"
                        aria-controls="navbarNav" aria-expanded="false" aria-label="Toggle navigation">
                        <span class="navbar-toggler-icon"></span>
                    </button>
                    <div class="collapse navbar-collapse" id="navbarNav">
                        <ul class="navbar-nav">
                            <!-- Home -->
                            <li class="nav-item dropdown">
                                <a class="nav-link dropdown-toggle" href="#" role="button" data-bs-toggle="dropdown"
                                    aria-expanded="false">
                                    Home
                                </a>
                                <ul class="dropdown-menu">
                                    <li v-for="(link, i) in homeLinks" :key="i">
                                        <a href="#"
                                            v-bind:class="link.active ? 'nav-link-active dropdown-item d-flex align-items-center' : 'dropdown-item d-flex align-items-center'">{{
                                                link.name }}
                                            <i class="fa-solid fa-star pb-1 ps-1" v-if="link.star === true"></i>
                                        </a>
                                    </li>
                                </ul>
                            </li>
                            <!-- Courses -->
                            <li class="nav-item dropdown">
                                <a class="nav-link dropdown-toggle" href="#" role="button" data-bs-toggle="dropdown"
                                    aria-expanded="false">
                                    Courses
                                </a>
                                <ul class="dropdown-menu my-show my-dropdown-center">
                                    <li v-for="section in coursesLinks" :key="section.subtitle">
                                        <p>{{ section.subtitle }}</p>
                                        <ul class="list-unstyled pe-5 pt-2">
                                            <li v-for="(link, i) in section.childsLink" :key="'link_' + i">
                                                <a class="dropdown-item" href="#" v-if="link.name">{{ link.name }}</a>
                                                <img class="nav-img" v-bind:src="`/public/img/${link.img}`" alt=""
                                                    v-if="link.img">
                                            </li>
                                        </ul>
                                    </li>
                                </ul>
                            </li>
                            <!-- Instructors -->
                            <li class="nav-item dropdown">
                                <a class="nav-link dropdown-toggle" href="#" role="button" data-bs-toggle="dropdown"
                                    aria-expanded="false">
                                    Instructors
                                </a>
                                <ul class="dropdown-menu">
                                    <li v-for="(link, i) in instructorsLinks" :key="i">
                                        <a href="#" class="dropdown-item"> {{ link.name }} </a>
                                    </li>
                                </ul>
                            </li>
                            <!-- Events -->
                            <li class="nav-item dropdown">
                                <a class="nav-link dropdown-toggle" href="#" role="button" data-bs-toggle="dropdown"
                                    aria-expanded="false">
                                    Events
                                </a>
                                <ul class="dropdown-menu">
                                    <li v-for="(link, i) in eventsLinks" :key="i">
                                        <a href="#" class="dropdown-item"> {{ link.name }} </a>
                                    </li>
                                </ul>
                            </li>
                            <!-- Pages -->
                            <li class="nav-item dropdown">
                                <a class="nav-link dropdown-toggle" href="#" role="button" data-bs-toggle="dropdown"
                                    aria-expanded="false">
                                    Pages
                                </a>
                                <ul class="dropdown-menu">
                                    <li v-for="link in pagesLinks" :key="link.name">
                                        <a href="#" class="dropdown-item"> {{ link.name }} </a>
                                    </li>
                                </ul>
                            </li>
                            <!-- Elements -->
                            <li class="nav-item dropdown">
                                <a class="nav-link dropdown-toggle" href="#" role="button" data-bs-toggle="dropdown"
                                    aria-expanded="false">
                                    Elements
                                </a>
                                <ul class="dropdown-menu my-show my-dropdown-center">
                                    <li v-for="section in elementsLinks" :key="section.subtitle">
                                        <p>{{ section.subtitle }}</p>
                                        <ul class="list-unstyled pe-1">
                                            <li v-for="(link, i) in section.childsLink" :key="'link_' + i">
                                                <a class="dropdown-item" href="#">{{ link.name }}</a>
                                            </li>
                                        </ul>
                                    </li>
                                </ul>
                            </li>
                        </ul>
                    </div>
                    <!-- Icone -->
                    <div class="my-icons-link ps-2">
                        <a href="#">
                            <i class="fa-solid fa-magnifying-glass fa-flip-horizontal ps-3"></i>
                        </a>
                        <a href="#">
                            <i class="fa-solid fa-bag-shopping pe-3"></i>
                        </a>
                        <a href="#">
                            <i class="fa-solid fa-bars"></i>
                        </a>
                    </div>
                </div>
            </div>
        </nav>
    </header>
</template>

<style lang="scss" scoped>
@use "../styles/partials/variables" as *;

.navbar-nav .nav-item.dropdown {
    position: relative;
}

.my-dropdown-center {
    position: absolute;
    right: 50%;
    transform: translateX(20%);
}

.nav-link, .my-icons-link > a {
    text-transform: uppercase;
    color: #ffffff;
    font-size: .9rem;

    &:hover,
    &:active,
    &:focus {
        color: $light-grey;
    }
}

.dropdown:hover .dropdown-menu {
    display: block;
}

.dropdown-toggle::after {
    display: none;
}

.dropdown-menu {
    text-align: left;
    list-style: none;
    background-color: #ffffff;
    background-clip: padding-box;
    border: none;
    border-top: 3px solid $primary-color;
    border-radius: 0;

    .dropdown-item {
        color: $light-grey;

        &:hover,
        &:active {
            color: $primary-color;
            text-decoration: none;
            background-color: #ffffff;
        }
    }

    a {
        font-size: .9rem;
    }

    i {
        font-size: .7rem;
        color: $primary-color;
    }

    p {
        color: $grey;
        font-weight: 700;
        padding: 4px 16px;
        margin: 0;
        font-size: .9rem;
    }
}

.dropdown:hover .my-show,
.dropdown:focus .my-show,
.dropdown:active .my-show {
    display: flex;
}

.nav-item .nav-link-active {
    color: $primary-color;
}

.nav-img {
    width: 200px;
}

.navbar-brand {
    img {
        width: 165px;
        height: 30px;
    }
}
</style>