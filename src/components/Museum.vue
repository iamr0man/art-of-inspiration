header<template>
  <div class="museum">
    <div class="museum__aside">
      <div class="museum__top">
        <h1 class="museum__number">01</h1>
        <p class="museum__additional">Tickets</p>
      </div>
      <img class="museum__image museum__image-right" src="../assets/photos/museum-medium.jpeg" alt="museum outside">
    </div>
    <div class="museum__main">
      <img class="museum__image museum__image-middle" src="../assets/photos/museum-small.jpeg" alt="Vincent van Gogh">
      <h2 class="museum__header"><span>van</span> <span>gogh</span> <span>museum</span></h2>
      <p class="museum__about">Step into Van Gogh's world. Explore the world's largest collection of works by Vincent van Gogh at the Van Gogh Museum in Amsterdam</p>
    </div>
    <div class="museum__section">
      <img class="museum__image museum__image-big" src="../assets/photos/news03.jpeg" alt="museum outside">
    </div>
  </div>   
</template>

<script>
export default {

}
</script>

<style lang="scss">
  .museum {
    width: 100vw;
    background-color:#fef6f0;
    display: flex;
    flex-direction: column;
    position: relative;

    &__aside {
      width: 80%;
      border-right: 2px solid #d7d3d0;
      display: flex;
      flex-direction: column;
      justify-content: center;  
      .museum__top {
        display: flex;
        justify-content: flex-start;
        align-items: baseline;
        .museum__number {
          font-family: 'Armin-Grotesk', sans-serif;
          text-shadow: -1px 0 #000, 0 1px #000, 1px 0 #000, 0 -1px #fff;
          color: #fef6f0;
          font-size: 100px;
        }

      }
      .museum__image {
        display: none;
      }
    }

    &__main {
      width: 80%;
      display: flex;
      flex-direction: column;
      justify-content: space-between;
      border-right: 2px solid #d7d3d0;
      
      .museum__header {
        display: flex;
        flex-direction: column;
        align-items: flex-end;
        text-transform: uppercase;
        font-size: 44px;
        z-index: 1;
      }

      .museum__about {
        color: #d7d3d0;
        padding: 10px;
        text-align: justify;
      }

      .museum__image {
        width: 255%;
        position: relative;
        right: 220px;
        z-index: 1;
      }
    }

    &__section {
      display: none;
    }
  }

  @media screen and (min-width: 1440px) {
    .museum {
      flex-direction: row;
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

      &__aside {
        order: 3;
        justify-content: space-between;
        border-right: none;

        .museum__image {
          display: block;
          width: 132%;
          margin-left: 17px;
        }
      }
      &__main {
        order: 2;
        border-right: none;
        .museum__image {
          width: 100%;
          right: 0;
          left: 160px;
          order: 3;
        }

        .museum__header {
          font-size: 94px;
        }
      }

      &__section {
        order: 1;
        display: block;

        .museum__image {
          width: 124%;
          margin-bottom: -77px;
        }
      }
    }
  }
</style>