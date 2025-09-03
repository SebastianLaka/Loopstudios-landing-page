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
        gridImage: ImageDeepEarth,
    },
    {
        id: 2,
        gridTitle: 'night arcade',
        gridDescription: 'Night arcade picture',
        gridImage: ImageNightArcade

    },
    {
        id: 3,
        gridTitle: 'soccer team vr',
        gridDescription: 'Soccer team vr picture',
        gridImage: ImageSoccerTeam
    },
    {
        id: 4,
        gridTitle: 'the grid',
        gridDescription: 'The grid picture',
        gridImage: ImageGrid
    },
    {
        id: 5,
        gridTitle: 'from up above vr',
        gridDescription: 'from up above vr picture',
        gridImage: ImageFromAbove
    },
    {
        id: 6,
        gridTitle: 'pocket borealis',
        gridDescription: 'pocket borealis picture',
        gridImage: ImagePocketBorealis
    },
    {
        id: 7,
        gridTitle: 'the curiosity',
        gridDescription: 'the curiosity picture',
        gridImage: ImageCuriosity
    },
    {
        id: 8,
        gridTitle: 'Make it fisheye',
        gridDescription: 'Fisheye picture',
        gridImage: ImageFisheye
    }
])

</script>
<template>
    <div class="grid-main">
        <GridCreations v-for="gridItem in gridData" :key="gridItem.id" :src="gridItem.gridImage" :title="gridItem.gridTitle"/>
    </div>
</template>
<style scoped lang="scss">
@media (min-width: 320px){
    .grid-main{
        display: flex;
        flex-direction: column;
        gap: 2em 0;
    }
}
</style>