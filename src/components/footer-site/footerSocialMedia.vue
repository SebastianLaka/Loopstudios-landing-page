<script setup>
const props = defineProps({
  src: String,
  alt: String,
})
</script>
<template>
  <a href="#" class="sm-icons"><img :src="props.src" :alt="props.alt" /></a>
</template>
<style scoped lang="scss">
@use '@/assets/sass/mixins' as *;
@use '@/assets/sass/colors' as *;
@use '@/assets/sass/fonts' as *;
@media (min-width: 320px) {
  .sm-icons {
    position: relative;
    font-weight: $secondary-font-weight;
    font-family: 'Alata', sans-serif;
    @include desktop-highlight;
  }
}
</style>
