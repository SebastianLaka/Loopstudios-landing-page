<script setup>
import HeaderCreations from './HeaderCreations.vue'
import { ref, onMounted } from 'vue'
const header = ref('')
const changeHeaderName = (title) => {
  return (header.value = title.toUpperCase())
}
onMounted(() => {
  const headerTitle = 'our creations'
  changeHeaderName(headerTitle)
})
</script>
<template>
  <section class="wrapper">
    <HeaderCreations>{{ header }}</HeaderCreations>
  </section>
</template>
<style scoped lang="scss"></style>
