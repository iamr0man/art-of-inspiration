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

  @media screen and (max-width: 1440px) {

    .meet {
      &__article {
      border-right: none;
      justify-content: space-between;
      align-items: center;

        .meet__header {
          font-size: 94px;
        }

        .meet__between {
          // display: block;
          // width: 30vw;
          // height: 100%;
          border-right: 2px solid #d7d3d0;
        }
      }

      &__item {
        display: flex;
        flex-direction: row-reverse;
        padding: 100px 0;
        .item__image {
          width: 50%;
        }

        .meet__between {
          display: block;
          width: 24vw;
          border-left: 2px solid #d7d3d0;
        }

        .item__details {
          padding: 20px;
          border-right: 2px solid #d7d3d0;
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