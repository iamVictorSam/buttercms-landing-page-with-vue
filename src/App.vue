<script setup>
import navbar from "./components/NavBarMain.vue";
// import HeaderComp from './components/HeaderComp.vue';
import HeaderMain from "./components/HeaderMain.vue";
import features from "./components/features.vue";
import about from "./components/about.vue";
import footerComp from "./components/footerComp.vue";
</script>

<template>
  <div class="relative">
    <!-- <navbar /> -->
    <HeaderMain />
    <features />
    <about />
    <footerComp />
  </div>
</template>

<style scoped></style>
