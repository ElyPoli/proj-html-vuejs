<script>
import TheHeader from "./components/TheHeader.vue";
import TheFooter from "./components/TheFooter.vue";
import MainCards from "./components/MainCards.vue";

export default {
    components: {
        TheHeader,
        TheFooter,
        MainCards,
    }
}
</script>

<template>
  <TheHeader></TheHeader>
  <main class="pt-5 pb-5">
    <MainCards></MainCards>
  </main>
  <TheFooter></TheFooter>
</template>

<style lang="scss"></style>