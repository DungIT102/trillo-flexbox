<script setup></script>

<template>
  <header class="header">
    <img src="@/assets/img/logo.png" alt="trillo logo" class="logo" />

    <form action="#" class="search">
      <input type="text" placeholder="Search hotels" class="search__input" />
      <button class="search__button">
        <svg class="search__icon">
          <use href="@/assets/img/sprite.svg#icon-magnifying-glass"></use>
        </svg>
      </button>
    </form>

    <nav class="user-nav">
      <div class="user-nav__icon-box">
        <svg class="user-nav__icon">
          <use href="@/assets/img/sprite.svg#icon-bookmark"></use>
        </svg>
        <span class="user-nav__notification">7</span>
      </div>
      <div class="user-nav__icon-box">
        <svg class="user-nav__icon">
          <use href="@/assets/img/sprite.svg#icon-chat"></use>
        </svg>
        <span class="user-nav__notification">13</span>
      </div>

      <div class="user-nav__user">
        <img src="@/assets/img/user.jpg" alt="User photo" class="user-nav__user-photo" />
        <span class="user-nav__user-name">Jonas</span>
      </div>
    </nav>
  </header>
</template>

<style lang="scss" scoped>
  .header {
    display: flex;
    height: 7rem;
    justify-content: space-between;
    align-items: center;

    font-size: 1.4rem;
    border-bottom: var(--line);
    background-color: var(--color-secondary);

    @media only screen and (max-width: $bp-smallest) {
      height: 11rem;
      flex-wrap: wrap;
      align-content: space-around;
    }
  }

  .logo {
    height: 3.25rem;
    margin-left: 2rem;
  }

  .search {
    display: flex;
    flex: 0 0 40%;
    align-items: center;
    justify-content: end; /* fix when we want to click search button, it's move to left */

    @media only screen and (max-width: $bp-smallest) {
      order: 1;
      flex: 0 0 100%;
      background-color: var(--color-grey-light-2);
    }

    &__icon {
      width: 2.25rem;
      height: 2.25rem;
      fill: var(--color-grey-dark-3);

      @media only screen and (max-width: $bp-smallest) {
        margin-right: 1rem;
      }
    }

    &__input {
      width: 80%;
      padding: 0.7rem 2rem;
      margin-right: -3.24rem;
      border: none;
      border-radius: 100px;

      font-family: inherit;
      font-size: inherit;
      color: inherit;
      background-color: var(--color-grey-light-2);

      transition: all 0.2s;

      &::placeholder {
        font-weight: 300;
        color: var(--color-grey-light-5);

        @media only screen and (max-width: $bp-large) {
          font-weight: 400;
        }
      }

      &:focus {
        width: 100%;
        outline: none;
        background-color: var(--color-grey-light-3);
      }
    }

    &__input:focus + &__button {
      background-color: var(--color-grey-light-3);
    }

    &__button {
      display: flex;
      border: none;
      background-color: var(--color-grey-light-2);

      &:focus {
        outline: none;
      }

      &:active {
        transform: translateY(2px);
      }
    }
  }

  .user-nav {
    display: flex;
    align-items: center;
    align-self: stretch; /* When hover, stretch the content */

    & > * {
      display: flex;
      align-items: center;
      height: 100%;
      padding: 0 2rem;

      cursor: pointer;
    }

    & > *:hover {
      background-color: var(--color-grey-light-2);
    }

    &__icon {
      width: 2.25rem;
      height: 2.25rem;
      fill: var(--color-grey-dark-2);
    }

    &__user-photo {
      height: 3.75rem;
      margin-right: 1rem;
      border-radius: 50%;
    }

    &__icon-box {
      position: relative;
    }

    &__notification {
      display: flex;
      align-items: center;
      justify-content: center;

      width: 1.75rem;
      height: 1.75rem;
      padding: 0.8rem;
      border-radius: 50%;

      position: absolute;
      top: 1.2rem;
      right: 1.2rem;

      font-size: 1rem;
      font-weight: 600;
      color: var(--color-secondary);
      background-color: var(--color-primary);

      @media only screen and (max-width: $bp-smallest) {
        top: 0rem;
        right: 1rem;
      }
    }
  }
</style>
