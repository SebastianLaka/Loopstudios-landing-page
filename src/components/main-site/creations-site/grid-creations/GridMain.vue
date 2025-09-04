<script setup>
import { ref, computed, onMounted, onUnmounted } from 'vue'
import GridCreations from './GridCreations.vue'
import ImageCuriosityMobile from '@/assets/images/mobile-images/image-curiosity.jpg'
import ImageDeepEarthMobile from '@/assets/images/mobile-images/image-deep-earth.jpg'
import ImageFisheyeMobile from '@/assets/images/mobile-images/image-fisheye.jpg'
import ImageFromAboveMobile from '@/assets/images/mobile-images/image-from-above.jpg'
import ImageGridMobile from '@/assets/images/mobile-images/image-grid.jpg'
import ImageNightArcadeMobile from '@/assets/images/mobile-images/image-night-arcade.jpg'
import ImagePocketBorealisMobile from '@/assets/images/mobile-images/image-pocket-borealis.jpg'
import ImageSoccerTeamMobile from '@/assets/images/mobile-images/image-soccer-team.jpg'

import ImageCuriosityDesktop from '@/assets/images/desktop-images/image-curiosity.jpg'
import ImageDeepEarthDesktop from '@/assets/images/desktop-images/image-deep-earth.jpg'
import ImageFisheyeDesktop from '@/assets/images/desktop-images/image-fisheye.jpg'
import ImageFromAboveDesktop from '@/assets/images/desktop-images/image-from-above.jpg'
import ImageGridDesktop from '@/assets/images/desktop-images/image-grid.jpg'
import ImageNightArcadeDesktop from '@/assets/images/desktop-images/image-night-arcade.jpg'
import ImagePocketBorealisDesktop from '@/assets/images/desktop-images/image-pocket-borealis.jpg'
import ImageSoccerTeamDesktop from '@/assets/images/desktop-images/image-soccer-team.jpg'

const gridData = ref([
  {
    id: 1,
    gridTitle: 'deep earth',
    gridDescription: 'Deep earth picture',
    gridImageMobile: ImageDeepEarthMobile,
    gridImageDesktop: ImageDeepEarthDesktop,
  },
  {
    id: 2,
    gridTitle: 'night arcade',
    gridDescription: 'Night arcade picture',
    gridImageMobile: ImageNightArcadeMobile,
    gridImageDesktop: ImageNightArcadeDesktop,
  },
  {
    id: 3,
    gridTitle: 'soccer team vr',
    gridDescription: 'Soccer team vr picture',
    gridImageMobile: ImageSoccerTeamMobile,
    gridImageDesktop: ImageSoccerTeamDesktop,
  },
  {
    id: 4,
    gridTitle: 'the grid',
    gridDescription: 'The grid picture',
    gridImageMobile: ImageGridMobile,
    gridImageDesktop: ImageGridDesktop,
  },
  {
    id: 5,
    gridTitle: 'from up above vr',
    gridDescription: 'from up above vr picture',
    gridImageMobile: ImageFromAboveMobile,
    gridImageDesktop: ImageFromAboveDesktop,
  },
  {
    id: 6,
    gridTitle: 'pocket borealis',
    gridDescription: 'pocket borealis picture',
    gridImageMobile: ImagePocketBorealisMobile,
    gridImageDesktop: ImagePocketBorealisDesktop,
  },
  {
    id: 7,
    gridTitle: 'the curiosity',
    gridDescription: 'the curiosity picture',
    gridImageMobile: ImageCuriosityMobile,
    gridImageDesktop: ImageCuriosityDesktop,
  },
  {
    id: 8,
    gridTitle: 'Make it fisheye',
    gridDescription: 'Fisheye picture',
    gridImageMobile: ImageFisheyeMobile,
    gridImageDesktop: ImageFisheyeDesktop,
  },
])

const windowWidth = ref(window.innerWidth)

const isMobile = computed(() => {
  return windowWidth.value < 992
})

onMounted(() => {
  window.addEventListener('resize', () => {
    windowWidth.value = window.innerWidth
  })
})

onUnmounted(() => {
  window.removeEventListener('resize', () => {
    windowWidth.value = window.innerWidth
  })
})
</script>
<template>
  <div class="grid-main">
    <GridCreations
      v-for="gridItem in gridData"
      :key="gridItem.id"
      :src="isMobile ? gridItem.gridImageMobile : gridItem.gridImageDesktop"
      :title="gridItem.gridTitle"
    />
  </div>
</template>
<style scoped lang="scss">
@media (min-width: 320px) {
  .grid-main {
    display: flex;
    flex-direction: column;
    gap: 2em 0;
  }
}
@media (min-width: 992px) {
  .grid-main {
    display: grid;
    grid-template-columns: repeat(4, 1fr);
    gap: 2em;
  }
}
</style>
