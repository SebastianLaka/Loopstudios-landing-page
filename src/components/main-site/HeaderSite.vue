<script setup>
import { ref, onMounted } from 'vue'
const headerTitle = ref('')
const changeTitleName = (title) => {
  return (headerTitle.value = title.toUpperCase())
}
onMounted(() => {
  const titleFromHeader = 'immersive experiences that deliver'
  changeTitleName(titleFromHeader)
})
</script>
<template>
  <section class="header-container">
    <div class="header-wrapper wrapper">
      <div class="header-content">
        <h1 class="header-content__title">
          {{ headerTitle }}
        </h1>
      </div>
    </div>
  </section>
</template>
<style scoped lang="scss">
@use '@/assets/sass/colors' as *;
@use '@/assets/sass/mixins' as *;
.header-container { 
  @include flex-center-items;
}
@media (min-width: 320px) {
  .header-container {
    height: 100svh;
    background-image: url(@/assets/images/mobile-images/image-hero.jpg);
    background-repeat: no-repeat;
    background-size: cover;
    padding: 0 1em;
    .header-content {
      border: 0.2em solid $main-white;
      padding: 1.75em;
      &__title {
        padding: 1.2em 0 0 0;
        font-size: 2rem;
        line-height: 125%;
      }
    }
  }
}
@media (min-width: 425px) {
  .header-container {
    .header-content {
      &__title {
        font-size: 2.5rem;
      }
    }
  }
}
@media (min-width: 992px) {
  .header-container {
    background-image: url(@/assets/images/desktop-images/image-hero.jpg);
    justify-content: start;
    height: 100dvh;
    .header-content {
      width: 65%;
      &__title {
        font-size: 4rem;
        padding: 0 2em 0 0;
      }
    }
  }
}
@media (min-width: 1200px) {
  .header-container {
    .header-content {
      &__title {
        font-size: 4.6rem;
      }
    }
  }
}
@media (min-width: 1440px){
    .header-container {
    .header-content {
      &__title {
        font-size: 5rem;
      }
    }
  }
}
</style>
