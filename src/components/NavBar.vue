<script setup>
const navLinks = [
  { id: 1, name: 'About' },
  { id: 2, name: 'Carrers' },
  { id: 3, name: 'Events' },
  { id: 4, name: 'Products' },
  { id: 5, name: 'Support' },
]

</script>
<template>
  <ul class="nav-names">
    <li
      v-for="navLink in navLinks"
      :key="navLink.id"
      v-text="navLink.name"
      class="nav-names__link"
    ></li>
  </ul>
</template>
<style scoped lang="scss">
@use '../assets/sass/colors' as *;
@use '../assets/sass/fonts' as *;
.nav-names {
  display: flex;
  flex-direction: column;
  justify-content: center;
  &__link {
    list-style: none;
    color: $main-white;
    font-size: 1.6rem;
    font-family: 'Alata', sans-serif;
    font-weight: 300;
    cursor: pointer;
  }
}
@media (min-width: 320px) and (max-width: 991px) {
  .nav-names {
    position: absolute;
    inset: 0;
    background-color: $main-black;
    min-height: 100dvh;
    z-index: -10;
    padding: 0 2em;
    gap: 1.25em 0;
  }
}
@media (min-width: 992px) {
  .nav-names {
    flex-direction: row;
    gap: 0em 2em;
    &__link {
      font-size: $primary-font-size;
    }
  }
}
</style>
