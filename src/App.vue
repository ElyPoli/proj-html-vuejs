<script>
import TheHeader from "./components/TheHeader.vue";
import TheFooter from "./components/TheFooter.vue";

export default {
    components: {
        TheHeader,
        TheFooter,
    }
}
</script>

<template>
  <TheHeader></TheHeader>
  <main>
    <p>Titolo</p>
    <h1>Titolo</h1>
  </main>
  <TheFooter></TheFooter>
</template>

<style lang="scss"></style>