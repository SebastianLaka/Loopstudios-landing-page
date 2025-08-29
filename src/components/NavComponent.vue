<script setup>
import NavLogo from './NavLogo.vue'
import NavIconHamburger from './NavIconHamburger.vue'
import NavIconClose from './NavIconClose.vue'
import NavBar from './NavBar.vue'
</script>
<template>
  <nav class="main-navigation">
    <NavLogo />
    <div class="nav-container">
      <NavIconHamburger />
      <NavIconClose />
      <NavBar />
    </div>
  </nav>
</template>
<style scoped lang="scss">
@media (min-width: 320px) {
  .main-navigation {
    display: flex;
    align-items: center;
  }
}
</style>
