<script>
import TheHeader from "./components/TheHeader.vue";
import TheFooter from "./components/TheFooter.vue";
import MainCards from "./components/MainCards.vue";
import MainPostSections from "./components/MainPostSections.vue";
import MainTestimonialsCaruosel from "./components/MainTestimonialsCaruosel.vue";

export default {
    components: {
        TheHeader,
        TheFooter,
        MainCards,
        MainPostSections,
        MainTestimonialsCaruosel,
    }
}
</script>

<template>
  <TheHeader></TheHeader>
  <main class="pt-5 pb-5">
    <MainCards></MainCards>
    <MainPostSections></MainPostSections>
    <MainTestimonialsCaruosel></MainTestimonialsCaruosel>
  </main>
  <TheFooter></TheFooter>
</template>

<style lang="scss"></style>