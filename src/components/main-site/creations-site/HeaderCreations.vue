<template>
    <h1 class="creations-header">
        <slot></slot>
    </h1>
    
</template>
<style scoped lang="scss">
@use '@/assets/sass/colors' as *;
.creations-header{
    color: $main-black;
}
</style>