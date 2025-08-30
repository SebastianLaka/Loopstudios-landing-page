<script setup>
import NavComponent from './components/NavComponent.vue'
</script>
<template>
  <main class="main-container wrapper">
    <NavComponent />
  </main>
</template>
<style lang="scss">
@use './assets/sass/_reset.scss' as *;
@use './assets/sass/fonts.scss' as *;
@use './assets/sass/colors.scss' as *;
@use './assets/sass/wrapper' as *;
body {
  background-color: blue;
  font-family: 'Josefin Sans', sans-serif;
  color: $main-white;
  position: relative;
}
</style>
