<script setup>
import { ref } from 'vue'
import NavLogo from './NavLogo.vue'
import NavToggleIcons from './NavToggleIcons.vue'
import NavBar from './NavBar.vue'
const isCollapsed = ref(false)
const toggleState = () => {
  isCollapsed.value = !isCollapsed.value
}
</script>
<template>
  <nav class="main-navigation wrapper">
    <NavLogo />
    <div class="nav-container">
      <NavToggleIcons @click="toggleState" />
      <NavBar />
    </div>
  </nav>
</template>
<style scoped lang="scss">
@media (min-width: 320px) {
  .main-navigation {
    display: flex;
    align-items: center;
    justify-content: space-between;
    padding: 2em;
    position: fixed;
    top: 0;
    left: 0;
    right: 0;
    z-index: 1000;
  }
}
</style>
