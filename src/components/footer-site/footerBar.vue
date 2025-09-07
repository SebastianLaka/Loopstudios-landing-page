<script setup>
const props = defineProps({
  title: String,
})
</script>
<template>
  <ul>
    <a href="#" class="footer-link"
      ><li class="footer-bar">{{ props.title }}</li></a
    >
  </ul>
</template>
<style scoped lang="scss">
@use '@/assets/sass/colors' as *;
@use '@/assets/sass/fonts' as *;
@use '@/assets/sass/mixins' as *;
.footer-link {
  text-decoration: none;
  color: $main-white;
  position: relative;
  font-size: $primary-font-size;
  font-weight: $secondary-font-weight;
  
 @include desktop-highlight;
  .footer-bar {
    list-style-type: none;
  }
}
</style>
