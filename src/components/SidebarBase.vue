<script setup></script>

<template>
  <nav class="sidebar">
    <ul class="side-nav">
      <li class="side-nav__item side-nav__item--active">
        <a href="#" class="side-nav__link">
          <svg class="side-nav__icon">
            <use href="@/assets/img/sprite.svg#icon-home"></use>
          </svg>
          <span>hotel</span>
        </a>
      </li>
      <li class="side-nav__item">
        <a href="#" class="side-nav__link">
          <svg class="side-nav__icon">
            <use href="@/assets/img/sprite.svg#icon-aircraft-take-off"></use>
          </svg>
          <span>flight</span>
        </a>
      </li>
      <li class="side-nav__item">
        <a href="#" class="side-nav__link">
          <svg class="side-nav__icon">
            <use href="@/assets/img/sprite.svg#icon-key"></use>
          </svg>
          <span>car rental</span>
        </a>
      </li>
      <li class="side-nav__item">
        <a href="#" class="side-nav__link">
          <svg class="side-nav__icon">
            <use href="@/assets/img/sprite.svg#icon-map"></use>
          </svg>
          <span>tours</span>
        </a>
      </li>
    </ul>

    <div class="legal">&copy; 2024 by Le Dung</div>
  </nav>
</template>

<style lang="scss" scoped>
  .sidebar {
    display: flex;
    flex-direction: column;
    flex: 0 0 18%;

    justify-content: space-between;
    background-color: var(--color-grey-dark-1);
  }

  .side-nav {
    list-style: none;
    font-size: 1.4rem;
    margin-top: 3.5rem;

    @media only screen and (max-width: $bp-medium) {
      display: flex;
      margin: 0;
    }

    &__item {
      position: relative;

      &:not(:last-child) {
        margin-bottom: 0.5rem;

        @media only screen and (max-width: $bp-medium) {
          margin: 0;
        }
      }

      @media only screen and (max-width: $bp-medium) {
        flex: 1;
      }
    }

    &__item::before {
      content: '';
      position: absolute;
      top: 0;
      left: 0;

      width: 3px;
      height: 100%;
      background-color: var(--color-primary);

      transform: scaleY(0);
      transition:
        transform 0.2s,
        background-color 0.1s,
        width 0.4s cubic-bezier(1, 0, 0, 1) 0.2s;
    }

    &__item:hover::before,
    &__item--active::before {
      transform: scaleY(1);
      width: 100%;
    }

    &__item:active::before {
      background-color: var(--color-primary-light);
    }

    &__link:link,
    &__link:visited {
      display: flex;
      padding: 1.5rem 3rem;
      align-items: center;

      position: relative; /* To position the pseudo element */
      z-index: 10;

      text-decoration: none;
      text-transform: uppercase;
      color: var(--color-grey-light-1);

      @media only screen and (max-width: $bp-medium) {
        justify-content: center;
        padding: 2rem;
      }

      @media only screen and (max-width: $bp-small) {
        flex-direction: column;
        padding: 1.5rem 0.5rem;
      }
    }

    &__icon {
      width: 1.75rem;
      height: 1.75rem;
      margin-right: 2rem;
      fill: currentColor;

      @media only screen and (max-width: $bp-small) {
        width: 1.5rem;
        height: 1.5rem;
        margin-right: 0;
        margin-bottom: 0.7rem;
      }
    }
  }

  .legal {
    padding: 2.5rem;
    font-size: 1.2rem;
    text-align: center;
    color: var(--color-grey-light-4);

    @media only screen and (max-width: $bp-medium) {
      display: none;
    }
  }
</style>
