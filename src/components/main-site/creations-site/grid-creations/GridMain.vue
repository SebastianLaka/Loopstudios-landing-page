<script setup>
import { ref } from 'vue';
import GridCreations from './GridCreations.vue';
import ImageCuriosity from "@/assets/images/mobile-images/image-curiosity.jpg";
import ImageDeepEarth from "@/assets/images/mobile-images/image-deep-earth.jpg";
import ImageFisheye from "@/assets/images/mobile-images/image-fisheye.jpg";
import ImageFromAbove from "@/assets/images/mobile-images/image-from-above.jpg";
import ImageGrid from "@/assets/images/mobile-images/image-grid.jpg";
import ImageInteractive from "@/assets/images/mobile-images/image-interactive.jpg";
import ImageNightArcade from "@/assets/images/mobile-images/image-night-arcade.jpg";
import ImagePocketBorealis from "@/assets/images/mobile-images/image-pocket-borealis.jpg";
import ImageSoccerTeam from "@/assets/images/mobile-images/image-soccer-team.jpg";

const gridData = ref([
    {
        id: 1,
        gridTitle: 'deep earth',
        gridDescription: 'Deep earth picture',
        gridImage: ImageDeepEarth
    },
])

</script>
<template>
    <div class="grid-main">
        <GridCreations v-for="gridItem in gridData" :key="gridItem.id" :src="gridItem.gridImage" :title="gridItem.gridTitle"/>
    </div>
</template>
<style scoped lang="scss"></style>