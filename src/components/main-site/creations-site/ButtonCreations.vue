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
        align-self: center;
        padding: 1em 3.5em;
        letter-spacing: .25em;
        text-transform: uppercase;
        font-family: inherit;
        font-weight: $secondary-font-weight;
        border: .2em solid $main-black;
        transition: background-color .3s, color .3s;
    }
    .grid-content-button:hover{
        background-color: $main-black;
        color: $main-white;
    }
}
</style>