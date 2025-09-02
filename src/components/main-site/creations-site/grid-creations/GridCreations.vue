<script setup>
import { reactive } from 'vue';
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
  objectfit: 'cover'
})
</script>
<template>
  <div class="grid-item">
    <h2 class="grid-item__name">{{ props.title }}</h2>
    <img :style="styleImage" :src="props.src" :alt="props.alt">
  </div>
</template>
<style scoped lang="scss">
.grid-item{
    position: relative;
    &__name{
        position: absolute;
        bottom: 50px;
        left: 25px;
        font-size: 1.6rem;
        inline-size: 3.5em;
        overflow-wrap: break-word;
        line-height: 125%;
        text-transform: uppercase;
    }
}
</style>
