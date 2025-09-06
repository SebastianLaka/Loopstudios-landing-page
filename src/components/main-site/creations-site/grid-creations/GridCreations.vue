<script setup>
import { reactive } from 'vue'
const props = defineProps({
  title: String,
  src: {
    type: String,
    required: true,
  },
  alt: String,
})

const styleImage = reactive({
  display: 'block',
  width: '100%',
  objectfit: 'cover',
})
</script>
<template>
  <div class="grid-item wrapper">
    <h2 class="grid-item__name">{{ props.title }}</h2>
      <img :style="styleImage" :src="props.src" :alt="props.alt" />
  </div>
</template>
<style scoped lang="scss">
@use '@/assets/sass/colors' as *;

@media (min-width: 320px) {
  .grid-item {
    position: relative;
    cursor: pointer;
    &__name {
      position: absolute;
      bottom: 0;
      left: 0;
      font-size: 1.6rem;
      inline-size: 7.5em;
      overflow-wrap: break-word;
      line-height: 125%;
      text-transform: uppercase;
      padding: 1em;
    }
    img{
      transition: background .3s ease-in, color .3s ease-in
    }
    img:hover{
      background: rgba($main-white, 0.3);
      color: $main-black;
    }
  }
}
@media (min-width: 992px) {
  .grid-item {
    &__name {
      padding: 2em;
      inline-size: 9.5em;
    }
  }
}
</style>
