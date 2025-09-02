<script setup>
import HeaderCreations from './HeaderCreations.vue'
import GridMain from './grid-creations/GridMain.vue'
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
  <section class="creations-section wrapper">
    <HeaderCreations>{{ header }}</HeaderCreations>
    <GridMain/>
  </section>
</template>
<style scoped lang="scss">

</style>
