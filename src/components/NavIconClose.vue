<script setup></script>
<template>
  <button class="close-icon">
    <img src="./icons/icon-close.svg" alt="Close menu" />
  </button>
</template>
<style scoped lang="scss">
.close-icon {
  background-color: transparent;
  border: none;
  padding: 0.5em;
  cursor: pointer;
}
@media (min-width: 992px) {
  .close-icon {
    display: none;
  }
}
</style>
