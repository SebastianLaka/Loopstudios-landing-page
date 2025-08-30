<script setup></script>
<template>
    <button class="hamburger-icon">
        <img src="./icons/icon-hamburger.svg" alt="Show menu">
    </button>
</template>
<style scoped lang="scss">
.hamburger-icon{
    background-color: transparent;
    border: none;
    padding: .5em;
    cursor: pointer;
}
@media (min-width: 992px) {
  .hamburger-icon {
    display: none;
  }
}
</style>
