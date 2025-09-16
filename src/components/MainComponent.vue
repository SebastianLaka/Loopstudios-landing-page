<script setup>
import HeaderSite from '../components/main-site/HeaderSite.vue';
import AboutSite from '../components/main-site/AboutSite.vue';
import ContentCreations from '../components/main-site/creations-site/ContentCreations.vue';
import footerComponent from '../components/footer-site/FooterComponent.vue';
</script>
<template>
  <main class="main-container">
    <HeaderSite />
    <AboutSite />
    <ContentCreations />
    <footerComponent />
  </main>
</template>
<style scoped lang="scss">
@use '@/assets/sass/mixins' as *;
@media(min-width: 320px){
  .main-container{
    @include flex-column;
    gap: 4em 0;
  }
}
</style>