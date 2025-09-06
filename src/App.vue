<script setup>
import MainComponent from './components/MainComponent.vue';
</script>
<template>
 <MainComponent />
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
