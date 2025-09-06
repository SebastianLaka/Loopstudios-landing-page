<script setup>
import footerLogo from './footerLogo.vue';
import footerRights from './footerRights.vue';
</script>
<template>
  <footer class="footer-container">
    <div class="footer-content wrapper">
      <footerLogo />
      <footerRights>
        © 2021 Loopstudios. All rights reserved.
      </footerRights>
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
