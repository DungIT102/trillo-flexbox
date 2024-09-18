<script setup>
  import DetailsBase from './components/DetailsBase.vue'
  import GalleryBase from './components/GalleryBase.vue'
  import HeaderBase from './components/HeaderBase.vue'
  import OverviewBase from './components/OverviewBase.vue'
  import SidebarBase from './components/SidebarBase.vue'
</script>

<template>
  <div class="container">
    <HeaderBase />

    <div class="content">
      <SidebarBase />

      <main class="hotel-view">
        <GalleryBase />
        <OverviewBase />
        <DetailsBase />
      </main>
    </div>
  </div>
</template>

<style lang="scss" scoped>
  .container {
    max-width: 120rem;
    min-height: 50rem;
    margin: 8rem auto;

    background-color: var(--color-grey-light-1);
    box-shadow: var(--shadow-dark);

    @media only screen and (max-width: $bp-largest) {
      margin: 0;
      max-width: 100%;
      width: 100%;
    }
  }

  .content {
    display: flex;

    @media only screen and (max-width: $bp-medium) {
      flex-direction: column;
    }
  }

  .hotel-view {
    flex: 1;
    background-color: var(--color-secondary);
  }
</style>
