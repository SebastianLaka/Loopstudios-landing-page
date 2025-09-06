<template>
  <p class="footer-rights"><slot></slot></p>
</template>
<style scoped lang="scss">
@use '@/assets/sass/colors' as *;
.footer-rights{
    color: $main-grey;
}
</style>
