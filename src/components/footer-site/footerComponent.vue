<script setup>
import footerLogo from './footerLogo.vue'
</script>
<template>
  <footer class="footer-container">
    <div class="footer-content wrapper">
      <footerLogo />
    
    </div>
  </footer>
</template>
<style scoped lang="scss">
@use '@/assets/sass/colors' as *;
.footer-container {
  background-color: $main-black;
  margin-top: 2em;
  padding: 2em 0;
}
</style>
