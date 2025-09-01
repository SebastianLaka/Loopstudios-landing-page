<script setup>
import { ref, Transition, onMounted, onUnmounted  } from 'vue'
import NavLogo from './NavLogo.vue'
import NavToggleIcons from './NavToggleIcons.vue'
import NavBar from './NavBar.vue'
const isMobile = ref(false)
const isDesktop = ref(null)

const toggleState = () => {
  isMobile.value = !isMobile.value;
}
const handleResize = () => {
  isDesktop.value = window.innerWidth >= 992;
}
onMounted(() => {
  handleResize(); 
  window.addEventListener('resize', handleResize);
})
onUnmounted(() => {
  window.removeEventListener('resize', handleResize);
})
</script>
<template>
  <nav class="main-navigation wrapper">
    <NavLogo />
    <div class="nav-container">
      <NavToggleIcons @toggle-nav="toggleState" :isToggle="isMobile" />
      <Transition name="slide-from-right">
        <NavBar v-if="isDesktop || isMobile" />
      </Transition>
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
  .nav-container {
    .slide-from-right-enter-active,
    .slide-from-right-leave-active {
      transition: transform 0.5s ease-in-out;
    }
    .slide-from-right-enter-from,
    .slide-from-right-leave-to {
      transform: translateX(100%);
    }
  }
}
@media (min-width: 992px){
  .main-navigation{
    padding: 2em 0;
  }
}
</style>
