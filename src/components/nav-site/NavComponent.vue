<script setup>
import { ref, Transition, onMounted, onUnmounted } from 'vue'
import NavLogo from './NavLogo.vue'
import NavToggleIcons from './NavToggleIcons.vue'
import NavBar from './nav-bars/NavBar.vue'
const isMobile = ref(false)
const isDesktop = ref(null)
const scrollPosition = ref(0)
const updateScrollPosition = () => {
  scrollPosition.value = window.scrollY;
}
const toggleState = () => {
  isMobile.value = !isMobile.value;
}
const handleResize = () => {
  isDesktop.value = window.innerWidth >= 992
}
onMounted(() => {
  handleResize()
  window.addEventListener('resize', handleResize)
  window.addEventListener('scroll', updateScrollPosition)
})
onUnmounted(() => {
  window.removeEventListener('resize', handleResize)
  window.removeEventListener('scroll', updateScrollPosition)
})
</script>
<template>
  <nav class="main-navigation" :class="{ 'change-nav-color': scrollPosition > 50 }">
    <div class="nav-container wrapper">
      <NavLogo />
      <NavToggleIcons @toggle-nav="toggleState" :isToggle="isMobile" />
      <Transition name="slide-from-right">
        <NavBar v-if="isDesktop || isMobile" />
      </Transition>
    </div>
  </nav>
</template>
<style scoped lang="scss">
@use '@/assets/sass/colors' as *;
@media (min-width: 320px) {
  .main-navigation {
    display: flex;
    align-items: center;
    justify-content: space-between;
    padding: 1.1em;
    position: fixed;
    top: 0;
    left: 0;
    right: 0;
    z-index: 1000;
  }
  .change-nav-color {
    background-color: rgba($main-black, 0.8);
    animation: showNavColor .3s;
  }
  .nav-container {
    display: flex;
    justify-content: space-between;
    .slide-from-right-enter-active,
    .slide-from-right-leave-active {
      transition: transform 0.3s ease-in-out;
    }
    .slide-from-right-enter-from,
    .slide-from-right-leave-to {
      transform: translateX(100%);
    }
  }
  @keyframes showNavColor{
    from{
      background-color: transparent;
    }to{
      background-color: rgba($main-black, 0.8);
    }
  }
}
@media (min-width: 992px) {
  .main-navigation {
    padding: 2em 0;
  }
}
</style>
