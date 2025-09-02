<template>
  <h1 class="creations-header">
    <slot></slot>
  </h1>
</template>
<style scoped lang="scss">
@use '@/assets/sass/colors' as *;
@media (min-width: 320px) {
  .creations-header {
    color: $main-black;
    font-size: 2rem;
  }
}
@media (min-width: 992px) {
  .creations-header {
    font-size: 2.5rem;
  }
}
</style>
