<script setup></script>

<template>
  <section class="detail">
    <div class="description">
      <p class="paragraph">
        Lorem ipsum dolor sit amet, consectetur adipisicing elit. Animi nisi dignissimos debitis
        ratione sapiente saepe. Accusantium cumque, quas, ut corporis incidunt deserunt quae
        architecto voluptate.
      </p>
      <p class="paragraph">
        Accusantium cumque, quas, ut corporis incidunt deserunt quae architecto voluptate delectus,
        inventore iure aliquid aliquam.
      </p>

      <ul class="list">
        <li class="list__item">Close to the beach</li>
        <li class="list__item">Breakfast included</li>
        <li class="list__item">Free airport shuttle</li>
        <li class="list__item">Free wifi in all rooms</li>
        <li class="list__item">Air conditioning and heating</li>
        <li class="list__item">Pets allowed</li>
        <li class="list__item">We speak all languages</li>
        <li class="list__item">Perfect for families</li>
      </ul>

      <div class="recommend">
        <p class="recommend__count">Lucy and 3 other friends recommend this hotel.</p>
        <div class="recommend__friends">
          <img src="../assets/img/user-3.jpg" alt="Friend 1" class="recommend__photo" />
          <img src="../assets/img/user-4.jpg" alt="Friend 2" class="recommend__photo" />
          <img src="../assets/img/user-5.jpg" alt="Friend 3" class="recommend__photo" />
          <img src="../assets/img/user-6.jpg" alt="Friend 4" class="recommend__photo" />
        </div>
      </div>

      <div class="cta">
        <h2 class="cta__book-now">Good news! We have 4 free rooms for your selected dates!</h2>
        <button class="btn">
          <span class="btn__visible">Book now</span>
          <span class="btn__invisible">Only 4 rooms left</span>
        </button>
      </div>
    </div>

    <div class="user-reviews">
      <figure class="review">
        <blockquote class="review__text">
          Lorem ipsum dolor sit amet, consectetur adipisicing elit. Fuga doloremque architecto dicta
          animi, totam, itaque officia ex.
        </blockquote>
        <figcaption class="review__user">
          <img src="../assets/img/user-1.jpg" alt="User 1" class="review__photo" />
          <div class="review__user-box">
            <p class="review__user-name">Nick Smith</p>
            <p class="review__user-date">Feb 23rd, 2017</p>
          </div>
          <div class="review__rating">7.8</div>
        </figcaption>
      </figure>

      <figure class="review">
        <blockquote class="review__text">
          Lorem ipsum dolor sit amet, consectetur adipisicing elit. Fuga doloremque architecto dicta
          animi.
        </blockquote>
        <figcaption class="review__user">
          <img src="../assets/img/user-2.jpg" alt="User 1" class="review__photo" />
          <div class="review__user-box">
            <p class="review__user-name">Mary Thomas</p>
            <p class="review__user-date">Sept 13th, 2017</p>
          </div>
          <div class="review__rating">9.3</div>
        </figcaption>
      </figure>

      <button class="btn-inline">Show all <span>&rarr;</span></button>
    </div>
  </section>
</template>

<style lang="scss" scoped>
  .detail {
    display: flex;
    padding: 4.5rem 1.6rem;
    border-bottom: var(--line);

    font-size: 1.4rem;
    background-color: var(--color-grey-light-1);

    @media only screen and (max-width: $bp-medium) {
      flex-direction: column;
    }
  }

  .description {
    flex: 0 0 60%;
    padding: 3rem;
    margin-right: 1.5rem;
    background-color: var(--color-secondary);
    box-shadow: var(--shadow-light);

    @media only screen and (max-width: $bp-medium) {
      margin-right: 0;
      margin-bottom: 3rem;
    }

    .paragraph:not(:last-of-type) {
      margin-bottom: 2rem;
    }

    .list {
      list-style: none;
      margin: 3rem 0 0.6rem 0;
      padding: 3rem 0;

      display: flex;
      flex-wrap: wrap;
      border-top: var(--line);

      &__item {
        flex: 0 0 50%;
        margin-bottom: 0.7rem;
      }

      &__item::before {
        content: '';
        display: inline-block;
        height: 1rem;
        width: 1rem;
        margin-right: 0.7rem;

        /* Older browsers */
        background-image: url(@/assets/img/chevron-thin-right.svg);
        background-size: cover;
        filter: $filter-color-primary;

        /* Newer browsers */
        @supports (-webkit-mask-image: url()) or (mask-image: url()) {
          background-image: none;
          filter: none;
          background-color: var(--color-primary);

          mask-image: url(@/assets/img/chevron-thin-right.svg);
          mask-size: cover;

          -webkit-mask-image: url(@/assets/img/chevron-thin-right.svg);
          -webkit-mask-size: cover;
        }
      }
    }

    .recommend {
      display: flex;
      align-items: center;

      font-size: 1.3rem;
      color: var(--color-grey-dark-3);

      &__count {
        margin-right: auto;
      }

      &__friends {
        display: flex;
      }

      &__photo {
        width: 4rem;
        height: 4rem;
        box-sizing: content-box;

        border-radius: 50%;
        border: 3px solid var(--color-secondary);

        &:not(:last-child) {
          margin-right: -2rem;
        }
      }
    }

    .cta {
      margin: 3rem 0;
      padding: 3.5rem 0;
      text-align: center;
      border-top: var(--line);

      @media only screen and (max-width: $bp-medium) {
        padding: 2.5rem 0;
      }

      &__book-now {
        margin-bottom: 2.5rem;

        font-size: 1.8rem;
        font-weight: 600;
        text-transform: uppercase;
      }
    }
  }

  .user-reviews {
    display: flex;
    flex: 1;
    flex-direction: column;
    align-items: center;

    .review {
      position: relative;
      padding: 3rem;
      margin-bottom: 3.5rem;
      overflow: hidden;

      background-color: var(--color-secondary);
      box-shadow: var(--shadow-light);

      @media only screen and (max-width: $bp-medium) {
        width: 100%;
        padding: 3rem;
      }

      &__text {
        margin-bottom: 2rem;
      }

      &__user {
        display: flex;
        align-items: center;
      }

      &__photo {
        width: 4.5rem;
        height: 4.5rem;
        border-radius: 50%;
        margin-right: 1.5rem;
      }

      &__user-box {
        font-size: 1.1rem;
        margin-right: auto;
      }

      &__user-name {
        font-weight: 600;
        text-transform: uppercase;
      }

      &__user-date {
        font-weight: 400;
        color: var(--color-grey-dark-4);
      }

      &__rating {
        font-size: 2.2rem;
        font-weight: 400;
        color: var(--color-primary);
      }

      &::before {
        content: '\201C';
        position: absolute;
        top: 0.2rem;
        left: -0.2rem;

        font-family: sans-serif;
        font-size: 10rem;
        line-height: 1;
        color: var(--color-grey-light-2);
      }
    }
  }
</style>
