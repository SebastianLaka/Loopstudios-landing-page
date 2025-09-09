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
@use '@/assets/sass/mixins' as *;
@media (min-width: 320px){
  .creations-section{
    @include flex-column;
    gap: 2em 0;
  }
}
@media (min-width: 992px){
  .creations-section{
    display: grid;
    grid-template-columns: repeat(2, 1fr);
    .grid-content-button{
      grid-column: 2/3;
      grid-row: 1/2;
      justify-self: end
    }
    .grid-main{
      grid-column: 1/3;
    }
  }

}
</style>
