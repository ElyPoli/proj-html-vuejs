<script>
export default {
    data() {
        return {
            tabsList: [
                {
                    title: "Learning Possibilities",
                    text: "Lorem ipsum gravida nibh vel velit auctor aliquetn sollicitudirem quibibendum auci elit cons equat ipsutis sem nibh id elit. Duis sed odio sit amet nibh vulputate cursus a sit amet mauris. Morbi accumsan ipsum velit. Nam nec tellus a odio tincidunt",
                    img: "tabs-icon-1.png",
                    pointslist: [
                        { point: "We enrich lives through learning.", },
                        { point: "Maximizing potential through individual attention.", },
                        { point: "The trusted name for specialized training.", },
                        { point: "People teach. People learn. This is where they connect.", },
                    ]
                },
                {
                    title: "Inspiring Minds",
                    text: "Lorem Ipsn gravida nibh vel velit auctor aliquetn sollicitudirem quibibendum auci elit cons equat ipsutis sem nibh id elit. Duis sed odio sit amet nibh vulputate cursus a sit amet mauris. Morbi accumsan ipsum velit. Nam nec tellus a odio tincidunt",
                    img: "tabs-icon-2.png",
                    pointslist: [
                        { point: "Maximizing potential through individual attention.", },
                        { point: "We enrich lives through learning.", },
                        { point: "People teach. People learn. This is where they connect.", },
                        { point: "The trusted name for specialized training.", },
                    ]
                },
                {
                    title: "Investing in Knowledge",
                    text: "Lorem Ipsn gravida nibh vel velit auctor aliquetn sollicitudirem quibibendum auci elit cons equat ipsutis sem nibh id elit. Duis sed odio sit amet nibh vulputate cursus a sit amet mauris. Morbi accumsan ipsum velit. Nam nec tellus a odio tincidunt",
                    img: "tabs-icon-3.png",
                    pointslist: [
                        { point: "We enrich lives through learning.", },
                        { point: "Maximizing potential through individual attention.", },
                        { point: "The trusted name for specialized training.", },
                        { point: "People teach. People learn. This is where they connect.", },
                    ]
                },
                {
                    title: "Secure Your Future",
                    text: "Lorem Ipsn gravida nibh vel velit auctor aliquetn sollicitudirem quibibendum auci elit cons equat ipsutis sem nibh id elit. Duis sed odio sit amet nibh vulputate cursus a sit amet mauris. Morbi accumsan ipsum velit. Nam nec tellus a odio tincidunt",
                    img: "tabs-icon-4.png",
                    pointslist: [
                        { point: "Maximizing potential through individual attention.", },
                        { point: "We enrich lives through learning.", },
                        { point: "People teach. People learn. This is where they connect.", },
                        { point: "The trusted name for specialized training.", },
                    ]
                },
                {
                    title: "Where Learning Begins",
                    text: "Lorem Ipsn gravida nibh vel velit auctor aliquetn sollicitudirem quibibendum auci elit cons equat ipsutis sem nibh id elit. Duis sed odio sit amet nibh vulputate cursus a sit amet mauris. Morbi accumsan ipsum velit. Nam nec tellus a odio tincidunt",
                    img: "tabs-icon-5.png",
                    pointslist: [
                        { point: "We enrich lives through learning.", },
                        { point: "Maximizing potential through individual attention.", },
                        { point: "The trusted name for specialized training.", },
                        { point: "People teach. People learn. This is where they connect.	", },
                    ]
                },
                {
                    title: "Knowledge is Power",
                    text: "Lorem Ipsn gravida nibh vel velit auctor aliquetn sollicitudirem quibibendum auci elit cons equat ipsutis sem nibh id elit. Duis sed odio sit amet nibh vulputate cursus a sit amet mauris. Morbi accumsan ipsum velit. Nam nec tellus a odio tincidunt",
                    img: "tabs-icon-6.png",
                    pointslist: [
                        { point: "Maximizing potential through individual attention.", },
                        { point: "We enrich lives through learning.", },
                        { point: "People teach. People learn. This is where they connect.", },
                        { point: "The trusted name for specialized training.", },
                    ]
                },
            ],
            tabsNavigation: [
                { title: "What We Do" },
                { title: "Degree Programme" },
                { title: "Career Achievements" },
                { title: "Personal Managment" },
                { title: "Steps To Success" },
                { title: "Knowledge Transfer" },
            ],
            currentTab: 0,
        }
    },
    methods: {
        btnChangeTab(index) {
            this.currentTab = index;
        }
    },
}
</script>

<template>
    <div class="container tabs-container">
        <div class="row gy-3">
            <div class="col-12 col-sm-3">
                <div class="tabs-navigation">
                    <ul class="list-group">
                        <li class="list-group-item" v-for="(navigation, i) in tabsNavigation" :key="i"
                            v-bind:class="(currentTab === i ? 'navigation navigation-active' : 'navigation')"
                            @click="btnChangeTab(i)">
                            {{ navigation.title }}
                        </li>
                    </ul>
                </div>
            </div>
            <div class="col-12 col-sm-9 d-flex align-items-center">
                <div v-for="(tab, i) in tabsList" :key="i"
                    v-bind:class="(currentTab === i ? 'tab-active tabs-card' : 'tabs-card')">
                    <h5 class="pb-3">{{ tab.title }}</h5>
                    <p class="pb-3">{{ tab.text }}</p>
                    <div class="row align-items-end">
                        <div class="col-8">
                            <ul class="list-unlisted p-0">
                                <li class="list-group-item" v-for="(elementList, z) in tab.pointslist" :key="z">
                                    <i class="fa-solid fa-check pe-1"></i>
                                    {{ elementList.point }}
                                </li>
                            </ul>
                        </div>
                        <div class="col-4">
                            <img v-bind:src="`/public/img/${tab.img}`" v-bind:alt="tab.title">
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
    padding-top: 7rem;
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
    display: none;

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

.tabs-card.tab-active {
    display: inline-block;
}

.navigation.navigation-active {
    border-left: 7px solid $primary-color;
    color: $primary-color;
}
</style>