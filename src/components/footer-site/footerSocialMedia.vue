<script setup>
const props = defineProps({
  src: String,
  alt: String,
})
</script>
<template>
  <img :src="props.src" :alt="props.alt"/>
</template>

