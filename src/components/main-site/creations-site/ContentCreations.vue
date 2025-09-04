<script setup>
import HeaderCreations from './HeaderCreations.vue'
import GridMain from './grid-creations/GridMain.vue'
import ButtonCreations from './ButtonCreations.vue'
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
    <GridMain />
    <ButtonCreations>see all</ButtonCreations>
  </section>
</template>
<style scoped lang="scss">
@media (min-width: 320px){
  .creations-section{
    display: flex;
    flex-direction: column;
    gap: 2em 0;
  }
}
</style>
