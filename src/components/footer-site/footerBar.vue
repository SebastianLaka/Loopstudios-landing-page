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
.footer-link {
  text-decoration: none;
  color: $main-white;
  .footer-bar {
    list-style-type: none;
  }
}
</style>
