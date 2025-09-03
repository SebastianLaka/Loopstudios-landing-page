<script setup>
</script>
<template>
    <button class="grid-content-button">
        <slot></slot>
    </button>
</template>
<style scoped lang="scss">
@use '@/assets/sass/fonts' as *;
@use '@/assets/sass/colors' as *;
@media (min-width: 320px){
    .grid-content-button{
        text-align: center;
        padding: 1em 3.5em;
        letter-spacing: .25em;
        text-transform: uppercase;
        cursor: pointer;
        font-family: inherit;
        font-weight: bold;
        border: .2em solid $main-black;
    }
}
</style>