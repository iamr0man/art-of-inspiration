<template>
  <div class="meet">
    <div class="meet__article">
      <h2 class="meet__header">Meet Vincent</h2>
      <div class="meet__between"></div>
      <h2 class="meet__number">02</h2>
    </div>
    <div class="meet__item">
      <div class="meet__between"></div>
      <img src="../assets/photos/gogh1.jpeg" alt="Vincent van Gogh" class="item__image">
      <div class="item__details">
        <h3 class="item__header">
          <span>Vincent Gogh's</span>
          <span>Life and Works</span>
        </h3>
        <p class="item__additional">
          History
        </p>
      </div>
    </div>
    <div class="meet__item">
      <div class="meet__between"></div>
      <img src="../assets/photos/gogh2.jpeg" alt="Vincent van Gogh" class="item__image">
      <div class="item__details">
        <h3 class="item__header">
          <span>Storiest about</span>
          <span>Van Gogh</span>
        </h3>
        <p class="item__additional">
          Discover more
        </p>
      </div>
    </div>
    <div class="meet__item">
      <div class="meet__between"></div>
      <img src="../assets/photos/gogh3.jpeg" alt="Vincent van Gogh" class="item__image">
      <div class="item__details">
        <h3 class="item__header">
          <span>Explore the</span>
          <span>collection</span>
        </h3>
        <p class="item__additional">
          Paintings and drawings
        </p>
      </div>
    </div>
  </div>  
</template>

<script>
export default {

}
</script>
  
<style lang="scss">
  .meet {
    width: 100vw;
    padding: 50px 0;
    background-color: #1e1e1e;
    display: flex;
    flex-direction: column;
    color: #fff;
    position: relative;

    .meet__between {
      display: none;
    }

    &__article {
      width: 80%;
      border-right: 2px solid #d7d3d0;
      display: flex;
      justify-content: flex-start;
      align-items: baseline;

      .meet__header{
        font-size: 55px;
      }

      .meet__number {
        color: #1e1e1e;
        text-shadow: -1px 0 #fff, 0 1px #fff, 1px 0 #fff, 0 -1px #fff;
        font-family: 'Armin-Grotesk', sans-serif;
        font-size: 60px;
      }
    }

    &__item {
      .item__image {
        width: 100%;
      }

      .item__details {
        padding: 20px;
      }

      .item__additional {
        color: #a5a5a5;
        margin-top: 10px;
        font-size: 12px;
      }
    }
  }

  @media screen and (min-width: 1440px) {

    .meet {
      &__article {
      border-right: none;
      justify-content: space-between;
      align-items: center;
      padding: 20px;

      &::before {
        content: '';
        width: 0;
        height: 100%;
        position: absolute;
        border: 1px solid #d7d3d0;
        top: 0;
        left: 472px;
      }

      &::after {
        content: '';
        width: 0;
        height: 100%;
        position: absolute;
        border: 1px solid #d7d3d0;
        top: 0;
        right: 538px;
      }

        .meet__header {
          font-size: 94px;
        }
      }

      &__item {
        display: flex;
        flex-direction: row-reverse;
        justify-content: space-evenly;
        padding: 100px 0;

        &:first-child {
          .item__image {
            margin-right: 73px;
          }
        }

        &:last-child {
          .item__image {
            margin-left: 32px;
          }
        }

        .item__image {
          width: 50%;
          z-index: 1;
        }

        .meet__between {
          display: block;
          width: 8.3vw;
        }

        .item__details {
          padding: 20px;
          font-size: 24px;
        }

        .item__additional {
          color: #a5a5a5;
          margin-top: 10px;
          font-size: 12px;
        }
      }
    }
  }
</style>