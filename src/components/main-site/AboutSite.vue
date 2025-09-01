<script setup></script>
<template>
  <section class="about-site-container wrapper">
    <div class="background-section">
      <img
        src="@/assets/images/mobile-images/image-interactive.jpg"
        alt=""
        class="background-section__mobile-image"
      />
      <img
        src="@/assets/images/desktop-images/image-interactive.jpg"
        alt=""
        class="background-section__desktop-image"
      />
    </div>
    <div class="content-section">
      <h1 class="content-section__header">THE LEADER IN INTERACTIVE VR</h1>
      <p class="content-section__description">
        Founded in 2011, Loopstudios has been producing world-class virtual reality projects for
        some of the best companies around the globe. Our award-winning creations have transformed
        businesses through digital experiences that bind to their brand.
      </p>
    </div>
  </section>
</template>
<style scoped lang="scss">
@use '@/assets/sass/colors' as *;
@use '@/assets/sass/fonts' as *;
.about-site-container {
  display: flex;
  flex-direction: column;
  padding: 8em 1em;
  gap: 2.25em 0;
  .content-section {
    display: flex;
    justify-content: center;
    align-items: center;
    flex-direction: column;
    &__header {
      padding-bottom: 0.7em;
      font-size: 2.5rem;
    }
    &__header,
    &__description {
      color: $main-black;
    }
  }
}
@media (min-width: 320px) {
  .background-section {
    &__mobile-image {
      object-fit: cover;
      display: block;
      width: 100%;
      height: 100%;
    }
    &__desktop-image {
      display: none;
    }
  }
  .content-section {
    &__header,
    &__description {
      text-align: center;
      line-height: 125%;
    }
    &__description {
      font-weight: $secondary-font-weight;
      padding: 0 2em;
    }
  }
}
@media (min-width: 992px) {
  .about-site-container {
    padding: 8em 0;
    flex-direction: row;
    align-items: end;
    .background-section {
      &__mobile-image {
        display: none;
      }
      &__desktop-image {
        object-fit: cover;
        display: block;
        width: 125%;
        height: 100%;
        position: relative;
        z-index: -1;
      }
    }
    .content-section {
      width: 45%;
      background-color: $main-white;
      padding: 3em 4em 0 4em;
      &__header{
        margin-bottom: 1em;
      }
      &__header,
      &__description{
        text-align: start;
        padding: 0;
        line-height: 150%;
      }
    }
  }
}
</style>
