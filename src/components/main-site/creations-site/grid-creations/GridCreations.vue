<script setup>
const props = defineProps({
  title: String,
  src: {
    type: String,
    required: true,
  },
  alt: String,
})
</script>
<template>
  <div class="grid-item" :title="props.title">
    <h2>{{ props.title }}</h2>
    <img :src="props.src" :alt="props.alt">
  </div>
</template>
<style scoped lang="scss">
</style>
