<script setup>
const props = defineProps({
  title: String,
})
</script>
<template>
  <a href="#" class="link"
    ><li>{{ props.title }}</li></a
  >
</template>
<style scoped lang="scss">
@use '@/assets/sass/colors' as *;
@use '@/assets/sass/fonts' as *;
@media (min-width: 320px) {
  .link {
    list-style: none;
    color: $main-white;
    font-size: 1.6rem;
    font-family: 'Alata', sans-serif;
    font-weight: 300;
    text-decoration: none;
    cursor: pointer;
  }
}
@media (min-width: 992px){
   .link {
      font-size: $primary-font-size;
    }
}
</style>
