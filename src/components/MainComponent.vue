<script setup>
import NavComponent from '../components/nav-site/NavComponent.vue';
import HeaderSite from '../components/main-site/HeaderSite.vue';
import AboutSite from '../components/main-site/AboutSite.vue';
import ContentCreations from '../components/main-site/creations-site/ContentCreations.vue';
import FooterComponent from '../components/footer-site/FooterComponent.vue';

</script>
<template>
  <main class="main-container">
    <NavComponent />
    <HeaderSite/>
    <AboutSite />
    <ContentCreations/>
    <FooterComponent/>
  </main>
</template>
<style scoped lang="scss">
@media(min-width: 320px){
  .main-container{
    display: flex;
    flex-direction: column;
    gap: 4em 0;
  }
}
</style>