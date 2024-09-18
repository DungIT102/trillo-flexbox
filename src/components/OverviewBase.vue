<script setup></script>

<template>
  <section class="overview">
    <h1 class="overview__heading">Hotel Las Palmas</h1>

    <div class="overview__stars">
      <svg class="overview__icon-star">
        <use href="@/assets/img/sprite.svg#icon-star"></use>
      </svg>
      <svg class="overview__icon-star">
        <use href="@/assets/img/sprite.svg#icon-star"></use>
      </svg>
      <svg class="overview__icon-star">
        <use href="@/assets/img/sprite.svg#icon-star"></use>
      </svg>
      <svg class="overview__icon-star">
        <use href="@/assets/img/sprite.svg#icon-star"></use>
      </svg>
      <svg class="overview__icon-star">
        <use href="@/assets/img/sprite.svg#icon-star"></use>
      </svg>
    </div>

    <div class="overview__location">
      <svg class="overview__icon-location">
        <use href="@/assets/img/sprite.svg#icon-location-pin"></use>
      </svg>
      <button class="btn-inline">Albufeira, Portugal</button>
    </div>

    <div class="overview__rating">
      <div class="overview__rating-average">8.6</div>
      <div class="overview__rating-count">429 votes</div>
    </div>
  </section>
</template>

<style lang="scss" scoped>
  .overview {
    display: flex;
    align-items: center;
    border-bottom: var(--line);

    &__icon-star,
    &__icon-location {
      width: 1.75rem;
      height: 1.75rem;
      fill: var(--color-primary);
    }

    &__heading {
      padding: 1.5rem 3rem;

      font-size: 2.25rem;
      font-weight: 300;
      text-transform: uppercase;
      letter-spacing: 1px;

      @media only screen and (max-width: $bp-small) {
        font-size: 1.8rem;
        padding: 1.25rem 2rem;
      }
    }

    &__stars {
      display: flex;
      margin-right: auto;
    }

    &__location {
      display: flex;
      align-items: center;
      font-size: 1.2rem;
    }

    &__icon-location {
      margin-right: 0.5rem;
    }

    &__rating {
      display: flex;
      flex-direction: column;
      align-items: center;
      justify-content: center;

      padding: 0 2.25rem;
      margin-left: 3rem;
      align-self: stretch;

      color: var(--color-secondary);
      background-color: var(--color-primary);

      @media only screen and (max-width: $bp-small) {
        padding: 0 1.5rem;
      }

      &-average {
        font-size: 2.25rem;
        font-weight: 300;
        margin-bottom: -3px;

        @media only screen and (max-width: $bp-small) {
          font-size: 1.8rem;
        }
      }

      &-count {
        font-size: 1rem;
        font-weight: 500;
        text-transform: uppercase;

        @media only screen and (max-width: $bp-small) {
          font-size: 0.9rem;
          font-weight: 600;
        }
      }
    }
  }
</style>
