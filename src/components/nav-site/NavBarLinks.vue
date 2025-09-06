<script setup>
const props = defineProps({
  title: String,
})
</script>
<template>
  <li class="nav-names__link">{{ props.title }}</li>
</template>
<style scoped lang="scss">
</style>
