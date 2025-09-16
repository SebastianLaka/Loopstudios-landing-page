<script setup>
import { ref, Transition, onMounted, onUnmounted } from 'vue'
import NavLogo from './NavLogo.vue'
import NavToggleIcons from './NavToggleIcons.vue'
import NavBar from './nav-bars/NavBar.vue'

const isMobile = ref(false)
const isDesktop = ref(true)
const props = defineProps(
  {isScrolled: Boolean}
)

const toggleState = () => {
  isMobile.value = !isMobile.value
}
const handleResize = () => {
  isDesktop.value = window.innerWidth >= 992
}
onMounted(() => {
  handleResize()
  window.addEventListener('resize', handleResize)
})
onUnmounted(() => {
  handleResize()
  window.removeEventListener('resize', handleResize)

})
</script>
<template>
  <nav  class="main-navigation" :class="{'change-nav-color': isScrolled}">
    <div class="nav-container wrapper">
      <NavLogo />
      <NavToggleIcons @toggle-nav="toggleState" :isToggle="isMobile" />
      <Transition name="slide-from-right">
        <NavBar v-if="isDesktop || isMobile" :isMobile="isMobile"/>
      </Transition>
    </div>
  </nav>
</template>
<style scoped lang="scss">
@use '@/assets/sass/colors' as *;
@use '@/assets/sass/mixins' as *;
 .change-nav-color {
    background-color: rgba($main-black, 0.8);
    animation: showNavColor 0.3s;
  }
@media (min-width: 320px) {
  .main-navigation {
    @include flex-center-between;
    padding: 1.1em;
    position: fixed;
    top: 0;
    left: 0;
    right: 0;
    z-index: 1000;
  }
  .nav-container {
    @include flex-center-between;
    .slide-from-right-enter-active,
    .slide-from-right-leave-active {
      transition: transform 0.3s ease-in-out;
    }
    .slide-from-right-enter-from,
    .slide-from-right-leave-to {
      transform: translateX(100%);
    }
  }
  @keyframes showNavColor {
    from {
      background-color: transparent;
    }
    to {
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
