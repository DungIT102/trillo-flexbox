<script setup></script>

<template>
  <section class="gallery">
    <figure class="gallery__item">
      <img src="@/assets/img/hotel-1.jpg" alt="photo of hotel 1" class="gallery__photo" />
    </figure>
    <figure class="gallery__item">
      <img src="@/assets/img/hotel-2.jpg" alt="photo of hotel 2" class="gallery__photo" />
    </figure>
    <figure class="gallery__item">
      <img src="@/assets/img/hotel-3.jpg" alt="photo of hotel 3" class="gallery__photo" />
    </figure>
  </section>
</template>

<style lang="scss" scoped>
  .gallery {
    display: flex;

    &__photo {
      display: block;
      width: 100%;
    }
  }
</style>
