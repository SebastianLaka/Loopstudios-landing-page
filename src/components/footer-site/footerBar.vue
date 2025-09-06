<script setup>
const props = defineProps({
  title: String,
})
</script>
<template>
  <li class="footer-bar">{{ props.title }}</li>
</template>
<style scoped lang="scss">
</style>
