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
    <img :style="styleImage" :src="props.src" :alt="props.alt" class="grid-item__image" />
  </div>
</template>
<style scoped lang="scss">
@use '@/assets/sass/colors' as *;
@media (min-width: 320px) {
  .grid-item {
    position: relative;
    transition: color 0.3s ease;
    &__name {
      position: absolute;
      bottom: 0;
      left: 0;
      font-size: 1.6rem;
      inline-size: 7.5em;
      overflow-wrap: break-word;
      text-transform: uppercase;
      padding: 1em;
      transition: color 0.3s ease-in;
    }
    &::before {
      content: '';
      position: absolute;
      top: 0;
      left: 0;
      width: 100%;
      height: 100%;
      background: rgba(0, 0, 0, 0);
      transition: background 0.3s ease, color .3s ease;
      z-index: 0;
    }
    &:hover {
      &::before {
        background: rgba($main-white, 0.4);
      }
    }
  }
  .grid-item:hover{
    color: $main-black;
  }
}
@media (min-width: 992px) {
  .grid-item {
    &__name {
      padding: 2em 0 2em 2em;
    }
  }
}
</style>
