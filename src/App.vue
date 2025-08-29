<script setup>
import NavComponent from "./components/NavComponent.vue";
</script>
<template>
<NavComponent/>
</template>
<style lang="scss">
@use './assets/sass/_reset.scss' as *;
@use './assets/sass/fonts.scss' as *;
@use './assets/sass/colors.scss' as *;
body{
  background-color: black;
  font-family: 'Josefin Sans', sans-serif;
  color: $main-white;
}
</style>
