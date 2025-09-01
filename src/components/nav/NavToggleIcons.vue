<script setup>
defineProps({
  isToggle: Boolean,
})
const emits = defineEmits(['toggle-nav'])

</script>
<template>
  <button class="site-icon" @click="$emit('toggle-nav')">
    <img src="./icons/icon-hamburger.svg" alt="Show menu" class="hamburger-ico" v-if="!isToggle"/>
    <img src="./icons/icon-close.svg" alt="Close menu" class="close-icon" v-else/>
  </button>
</template>
<style scoped lang="scss">
.site-icon {
  background-color: transparent;
  border: none;
  padding: 0.5em;
  cursor: pointer;
}
@media (min-width: 992px) {
  .site-icon{
    display: none;
  .hamburger-icon, .close-icon {
    display: none;
  }
}
}
</style>
