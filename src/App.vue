<script setup>
import NavComponent from './components/NavComponent.vue';
import HeaderSite from './components/HeaderSite.vue';
</script>
<template>
  <main class="main-container">
    <NavComponent />
    <HeaderSite/>
  </main>
</template>
<style lang="scss">
@use './assets/sass/_reset.scss' as *;
@use './assets/sass/fonts.scss' as *;
@use './assets/sass/colors.scss' as *;
@use './assets/sass/wrapper' as *;
body {
  font-family: 'Josefin Sans', sans-serif;
  color: $main-white;
  position: relative;
}
</style>
