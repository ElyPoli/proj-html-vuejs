<script>
export default {
}
</script>

<template>
    <div class="geometric-bg">
        <div class="container pt-5 pb-5">
            <div class="text-center pt-2 pb-5">
                <h4 class="pb-3">Pricing Plans</h4>
                <p>
                    Lorem ipsum gravida nibh vel velit auctor aliquetnean sollicitudin, lorem quis bibendum auci
                </p>
            </div>
            <!-- Tabella -->
            <table class="table table-bordered pricing-plans-table">
                <thead>
                    <tr>
                        <th scope="col">
                            <h6>
                                Save up to 40% by paying weekly
                            </h6>
                        </th>
                        <th scope="col">
                            <img src="/public/img/pricing-plans-1.png" alt="Standard">
                            <h6>Standard</h6>
                            <p>$12</p>
                        </th>
                        <th scope="col" class="my-col-selected">
                            <img src="/public/img/pricing-plans-2.png" alt="Professional">
                            <h6>Professional</h6>
                            <p>$59</p>
                        </th>
                        <th scope="col">
                            <img src="/public/img/pricing-plans-3.png" alt="Advanced">
                            <h6>Advanced</h6>
                            <p>$88</p>
                        </th>
                    </tr>
                </thead>
                <tbody>
                    <tr>
                        <td>Number of Courses</td>
                        <td>2</td>
                        <td>4</td>
                        <td>6</td>
                    </tr>
                    <tr>
                        <td>Time</td>
                        <td>15 Days</td>
                        <td>30 Days</td>
                        <td>30 Days</td>
                    </tr>
                    <tr>
                        <td>Web Designing</td>
                        <td><i class="fa-solid fa-check"></i></td>
                        <td><i class="fa-solid fa-check"></i></td>
                        <td><i class="fa-solid fa-check"></i></td>
                    </tr>
                    <tr>
                        <td>Human-Centered Design</td>
                        <td><i class="fa-solid fa-check"></i></td>
                        <td><i class="fa-solid fa-check"></i></td>
                        <td><i class="fa-solid fa-check"></i></td>
                    </tr>
                    <tr>
                        <td>Basic Marketing</td>
                        <td><i class="fa-solid fa-xmark"></i></td>
                        <td><i class="fa-solid fa-check"></i></td>
                        <td><i class="fa-solid fa-check"></i></td>
                    </tr>
                    <tr>
                        <td>Python for Everybody</td>
                        <td><i class="fa-solid fa-xmark"></i></td>
                        <td><i class="fa-solid fa-check"></i></td>
                        <td><i class="fa-solid fa-check"></i></td>
                    </tr>
                    <tr>
                        <td>Android Developer</td>
                        <td><i class="fa-solid fa-xmark"></i></td>
                        <td><i class="fa-solid fa-xmark"></i></td>
                        <td><i class="fa-solid fa-check"></i></td>
                    </tr>
                    <tr>
                        <td>Business English</td>
                        <td><i class="fa-solid fa-xmark"></i></td>
                        <td><i class="fa-solid fa-xmark"></i></td>
                        <td><i class="fa-solid fa-check"></i></td>
                    </tr>
                    <tr>
                        <td class="empty-cell"></td>
                        <td class="pricing-plans-btn-box">
                            <button type="button" class="btn my-btn my-btn-unselected">Get it now</button>
                        </td>
                        <td class="pricing-plans-btn-box">
                            <button type="button" class="btn my-btn">Get it now</button>
                        </td>
                        <td class="pricing-plans-btn-box">
                            <button type="button" class="btn my-btn my-btn-unselected">Get it now</button>
                        </td>
                    </tr>
                </tbody>
            </table>
        </div>
    </div>
</template>

<style lang="scss" scoped>
@use "../styles/partials/variables" as *;

.geometric-bg {
    border-top: 1px solid $background-light;
    border-bottom: 1px solid $background-light;
}

h4 {
    font-size: $section-title-size;
}

.table {
    border-color: $background-light;
}

.pricing-plans-table {
    border-top: 3px solid rgba(64, 195, 255, 0.2);
    text-align: center;
    table-layout: fixed;

    .my-col-selected {
        border-top: 3px solid $primary-color;
    }

    h6 {
        font-size: 1.5rem;
        font-weight: bold;
    }

    img {
        padding-top: 2rem;
        padding-bottom: 2rem;
    }

    .fa-check {
        color: $primary-color;
    }

    td {
        color: $light-grey;
        padding-top: 1rem;
        padding-bottom: 1rem;

        &:first-of-type {
            text-align: left;
            padding-left: 2rem;
            font-weight: bold;
            font-family: Merriweather, serif;
        }
    }

    th {
        background-color: $primary-color-light;

        &:first-of-type {
            background-color: #ffffff;
            text-align: left;
            padding-left: 2rem;
            padding-bottom: 1.5rem;
        }
    }
}

.empty-cell {
    background-color: transparent;
}

.my-btn {
    padding: 1rem 2.3rem;
    margin: .8rem;
}

.pricing-plans-btn-box {
    background-color: $primary-color-light;
}

.my-btn-unselected {
    background-color: #ffffff;
    border: 1px solid $background-light;
    color: $light-grey;
    transition: all .3s;

    &:hover,
    &:active,
    &:focus {
        background-color: $primary-color !important;
        color: #ffffff !important;
    }
}
</style>