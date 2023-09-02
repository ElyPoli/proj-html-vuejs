<script>
export default {
    data() {
        return {
            listNavLinks: [
                {
                    title: "Home",
                    subheading: "",
                    secondLevelMenu: [
                        { name: "Home 1", star: false, active: false, thirdLevelMenu: "" },
                        { name: "Home 2", star: true, active: false, thirdLevelMenu: "" },
                        { name: "Home 3", star: false, active: false, thirdLevelMenu: "" },
                        { name: "Home 4", star: true, active: false, thirdLevelMenu: "" },
                        { name: "Home 5", star: false, active: false, thirdLevelMenu: "" },
                        { name: "Home 6", star: false, active: false, thirdLevelMenu: "" },
                        { name: "Home 7", star: false, active: false, thirdLevelMenu: "" },
                        { name: "Home 8", star: false, active: false, thirdLevelMenu: "" },
                        { name: "Home 9", star: false, active: false, thirdLevelMenu: "" },
                        { name: "Home 10", star: true, active: true, thirdLevelMenu: "" },
                        { name: "Home 11", star: false, active: false, thirdLevelMenu: "" },
                        { name: "Home 12", star: true, active: false, thirdLevelMenu: "" },
                        { name: "Landing", star: false, active: false, thirdLevelMenu: "" },
                    ],
                },
                {
                    title: "Courses",
                    subheading: [
                        {
                            name: "Features",
                            secondLevelColumn: [
                                { name: "All Courses", img: "", pay: "", free: "" },
                                { name: "Standard List", img: "", pay: "", free: "" },
                                { name: "Course Single", img: "", pay: "", free: "" },
                                { name: "User dashboard", img: "", pay: "", free: "" },
                            ],
                        },
                        {
                            name: "Business",
                            secondLevelColumn: [
                                { name: "", img: "courses-carousel-4.jpg", pay: "$40", free: "" },
                            ],
                        },
                        {
                            name: "Languages",
                            secondLevelColumn: [
                                { name: "", img: "courses-carousel-1.jpg", pay: "$20", free: "" },
                            ],
                        },
                        {
                            name: "Programming",
                            secondLevelColumn: [
                                { name: "", img: "courses-carousel-2.jpg", pay: "", free: "Free" },
                            ],
                        },
                    ],
                    secondLevelMenu: "",
                },
                {
                    title: "Instructors",
                    subheading: "",
                    secondLevelMenu: [
                        { name: "Become an Instructor", star: false, active: false, thirdLevelMenu: "" },
                        { name: "Instructor Single", star: false, active: false, thirdLevelMenu: "" },
                    ],
                },
                {
                    title: "Events",
                    subheading: "",
                    secondLevelMenu: [
                        { name: "Events Calendar", star: false, active: false, thirdLevelMenu: "" },
                        { name: "Events List", star: false, active: false, thirdLevelMenu: "" },
                        { name: "Event Single", star: false, active: false, thirdLevelMenu: "" },
                    ],
                },
                {
                    title: "Pages",
                    subheading: "",
                    secondLevelMenu: [
                        { name: "About", star: false, active: false, thirdLevelMenu: "" },
                        { name: "Gallery", star: false, active: false, thirdLevelMenu: "" },
                        { name: "Pricing Plan", star: false, active: false, thirdLevelMenu: "" },
                        {
                            name: "Blog", star: false, active: false,
                            thirdLevelMenu: [
                                { name: "Standard List" },
                                { name: "Masonry List" },
                                { name: "Blog Split" },
                                { name: "Standard Post" },
                                { name: "Quote Post" },
                                { name: "Link Post" },
                                { name: "Audio Post" },
                                { name: "Video Post" },
                            ],
                        },
                        {
                            name: "Shop", star: false, active: false,
                            thirdLevelMenu: [
                                { name: "Shop List" },
                                { name: "Standard Product" },
                                { name: "Grouped Product" },
                                { name: "External Product" },
                                { name: "Variable Product" },
                                { name: "Three Columns Grid" },
                                { name: "Three Columns Wide" },
                                { name: "Four Columns Grid" },
                                { name: "Four Columns Wide" },
                                { name: "Five Columns Grid" },
                                { name: "Five Columns Wide" },
                                { name: "My account" },
                                { name: "Cart" },
                                { name: "Checkout" },
                            ],
                        },
                        {
                            name: "Forums", star: false, active: false,
                            thirdLevelMenu: [
                                { name: "All Forums" },
                                { name: "Forum Topic" },
                            ],
                        },
                        { name: "Contact", star: false, active: false, thirdLevelMenu: "" },
                        { name: "FAQ", star: false, active: false, thirdLevelMenu: "" },
                        { name: "Coming Soon", star: false, active: false, thirdLevelMenu: "" },
                        { name: "Error Page", star: false, active: false, thirdLevelMenu: "" },
                    ],
                },
                {
                    title: "Elements",
                    subheading: [
                        {
                            name: "Course Shortcodes",
                            secondLevelColumn: [
                                { name: "Course List", img: "", pay: "", free: "" },
                                { name: "Course Slider", img: "", pay: "", free: "" },
                                { name: "Course Table", img: "", pay: "", free: "" },
                                { name: "Course Features", img: "", pay: "", free: "" },
                                { name: "Instructor List", img: "", pay: "", free: "" },
                                { name: "Instructor Slider", img: "", pay: "", free: "" },
                                { name: "Education Timeline", img: "", pay: "", free: "" },
                                { name: "Advanced Course Search", img: "", pay: "", free: "" },
                                { name: "Link Image List", img: "", pay: "", free: "" },
                            ],
                        },
                        {
                            name: "Classic",
                            secondLevelColumn: [
                                { name: "Accordions & Toggles", img: "", pay: "", free: "" },
                                { name: "Tabs", img: "", pay: "", free: "" },
                                { name: "Buttons", img: "", pay: "", free: "" },
                                { name: "Call To Action", img: "", pay: "", free: "" },
                                { name: "Contact Form", img: "", pay: "", free: "" },
                                { name: "Separators", img: "", pay: "", free: "" },
                                { name: "Icon Width Text", img: "", pay: "", free: "" },
                                { name: "Blockquote", img: "", pay: "", free: "" },
                                { name: "Typography", img: "", pay: "", free: "" },
                            ],
                        },
                        {
                            name: "Course Shortcodes",
                            secondLevelColumn: [
                                { name: "Couunters", img: "", pay: "", free: "" },
                                { name: "Countdown", img: "", pay: "", free: "" },
                                { name: "Pie Charts", img: "", pay: "", free: "" },
                                { name: "Google Maps", img: "", pay: "", free: "" },
                                { name: "Process", img: "", pay: "", free: "" },
                                { name: "Progress Bar", img: "", pay: "", free: "" },
                                { name: "Events List", img: "", pay: "", free: "" },
                                { name: "Pricing Tables", img: "", pay: "", free: "" },
                                { name: "Comparison Pricing Tables", img: "", pay: "", free: "" },
                            ],
                        },
                        {
                            name: "Presentation",
                            secondLevelColumn: [
                                { name: "Team Shortcode", img: "", pay: "", free: "" },
                                { name: "Testimonials", img: "", pay: "", free: "" },
                                { name: "Clients", img: "", pay: "", free: "" },
                                { name: "Blog List Shortcode", img: "", pay: "", free: "" },
                                { name: "Twitter List", img: "", pay: "", free: "" },
                                { name: "Product List", img: "", pay: "", free: "" },
                                { name: "Image Gallery", img: "", pay: "", free: "" },
                                { name: "Masonry Gallery", img: "", pay: "", free: "" },
                                { name: "Video Button", img: "", pay: "", free: "" },
                            ],
                        },
                    ],
                    secondLevelMenu: "",
                },
            ],
        };
    },
}
</script>

<template>
    <header>
        <div class="header-slider">
            <i class="fa-solid fa-chevron-left"></i>
            <div class="header-slider-text">
                <h2>Accelerate Your Career</h2>
                <p>
                    Lorem ipsum dolor sit amet consectetur adipisicing elit. Ad sint necessitatibus magni deleniti ut ipsa
                    ullam unde, exercitationem amet nisi.
                </p>
                <button type="button" class="btn my-btn mt-5">Register now</button>
            </div>
            <i class="fa-solid fa-chevron-right"></i>
        </div>
        <!-- Menu di navigazione -->
        <nav class="navbar navbar-expand-lg">
            <div class="container d-flex align-items-center justify-content-between">
                <div>
                    <a class="navbar-brand" href="#">
                        <img src="/public/img/logo-light.png" alt="iAcademy">
                    </a>
                </div>
                <div class="d-flex align-items-center">
                    <button class="navbar-toggler" type="button" data-bs-toggle="collapse"
                        data-bs-target="#navbarSupportedContent" aria-controls="navbarSupportedContent"
                        aria-expanded="false" aria-label="Toggle navigation">
                        <span class="navbar-toggler-icon"></span>
                    </button>
                    <div class="collapse navbar-collapse" id="navbarSupportedContent">
                        <ul class="navbar-nav me-auto mb-2 mb-lg-0">
                            <li class="nav-item dropdown" v-for="menuSection in listNavLinks" :key="menuSection.title">
                                <a class="nav-link dropdown-toggle" href="#" role="button" data-bs-toggle="dropdown"
                                    aria-expanded="false">
                                    {{ menuSection.title }}
                                </a>
                                <ul class="dropdown-menu my-dropdown-center" aria-labelledby="navbarDropdownMenuLink">
                                    <!-- Menù di secondo livello semplice -->
                                    <li class="open-third-level" v-for="(secondLevelLink, i) in menuSection.secondLevelMenu"
                                        :key="i" v-if="menuSection.secondLevelMenu">
                                        <a href="#"
                                            v-bind:class="secondLevelLink.active ? 'nav-link-active dropdown-item d-flex align-items-center' : 'dropdown-item d-flex align-items-center'">
                                            {{ secondLevelLink.name }}
                                            <i class="fa-solid fa-star pb-1 ps-1" v-if="secondLevelLink.star === true"></i>
                                        </a>
                                        <!-- Menù di terzo livello semplice -->
                                        <ul class="dropdown-menu dropdown-submenu third-level-link"
                                            v-if="secondLevelLink.thirdLevelMenu">
                                            <li v-for="(thirdLevelLink, a) in secondLevelLink.thirdLevelMenu" :key="a">
                                                <a class="dropdown-item" href="#">
                                                    {{ thirdLevelLink.name }}
                                                </a>
                                            </li>
                                        </ul>
                                    </li>
                                    <!-- Menù di secondo livello a colonne -->
                                    <li>
                                        <ul class="items-flex list-unstyled">
                                            <li v-for="(column, z) in menuSection.subheading" :key="z"
                                                v-if="menuSection.subheading">
                                                <p class="dropdown-item" href="#">{{ column.name }}</p>
                                                <ul class="list-unstyled pe-5 pt-2">
                                                    <li v-for="(link, x) in column.secondLevelColumn" :key="x">
                                                        <a class="dropdown-item" href="#" v-if="link.name">{{ link.name
                                                        }}</a>
                                                        <img class="nav-img" v-bind:src="`/public/img/${link.img}`" alt=""
                                                            v-if="link.img">
                                                        <div class="pt-2">
                                                            <span class="badge rounded-pill my-badge my-badge-blue"
                                                                v-if="link.pay">
                                                                {{ link.pay }}
                                                            </span>
                                                            <span
                                                                class="badge rounded-pill my-badge my-badge-yellow text-uppercase"
                                                                v-if="link.free">
                                                                {{ link.free }}
                                                            </span>
                                                        </div>
                                                    </li>
                                                </ul>
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

p,
h2 {
    color: white;
}

header {
    position: relative;
    background-image: url("/public/img/header-slide-1.jpg");
    height: 880px;
}

.header-slider {
    width: 100%;

    .header-slider-text,
    i {
        position: absolute;
        color: white;
    }

    .header-slider-text {
        top: 50%;
        left: 50%;
        transform: translate(-50%, -50%);
        text-align: center;

        h2 {
            font-size: 4.5rem;
            margin: 0;
            padding-bottom: 1.3rem;
        }

        p {
            font-size: 1.3rem;
            margin: 0;
        }
    }

    i {
        font-size: 3rem;
        top: 50%;
        transform: translateY(-50%);
        transition: color .3s;
        cursor: pointer;

        &:hover {
            color: $light-grey;
        }
    }

    i:first-child {
        padding-left: 2rem;
        left: 0;
    }

    i:last-child {
        padding-right: 2rem;
        right: 0;
    }
}

.dropdown-menu li {
    position: relative;
}

.dropdown-menu .dropdown-submenu {
    display: none !important;
    position: absolute;
    left: 100%;
    top: -7px;
}

.dropdown-menu .dropdown-submenu-left {
    right: 100%;
    left: auto;
}

.dropdown:hover .items-flex {
    display: flex !important;
    justify-content: center;
}

.open-third-level:hover .third-level-link {
    display: block !important;
}

.navbar {
    padding-top: 2rem;
}

.navbar-nav .nav-item.dropdown {
    position: relative;
    padding-left: 1.3rem;
    padding-right: 1.3rem;
}

.my-dropdown-center {
    position: absolute;
    right: 50%;
    transform: translateX(45%);
}

.nav-link,
.my-icons-link>a {
    text-transform: uppercase;
    color: #ffffff;
    font-size: .9rem;
    font-weight: bold;

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
        height: 32px;
    }
}
</style>