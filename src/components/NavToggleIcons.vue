<script setup>
const isClose = defineProps({
  isToggle: Boolean,
})
</script>
<template>
  <button class="hamburger-icon" v-if="isToggle">
    <img src="./icons/icon-hamburger.svg" alt="Show menu" />
  </button>
  <button class="close-icon" v-else>
    <img src="./icons/icon-close.svg" alt="Close menu" />
  </button>
</template>
<style scoped lang="scss">
.hamburger-icon, .close-icon {
  background-color: transparent;
  border: none;
  padding: 0.5em;
  cursor: pointer;
}
@media (min-width: 992px) {
  .hamburger-icon, .close-icon {
    display: none;
  }
}
</style>
