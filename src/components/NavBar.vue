<script setup>
const navLinks = [
    {id: 1, name: 'About'},
    {id: 2, name: 'Carrers'},
    {id: 3, name: 'Events'},
    {id: 4, name: 'Products'},
    {id: 5, name: 'Support'},
]
</script>
<template>
    <ul class="nav-names">
        <li v-for="navLink in navLinks" :key="navLink.id" v-text="navLink.name" class="nav-names__link"></li>
    </ul>
</template>
<style scoped lang="scss">
.nav-names{
    display: flex;
    flex-direction: column;
    &__link{
        list-style: none;
        padding: 0 .5em;
    }
}
</style>