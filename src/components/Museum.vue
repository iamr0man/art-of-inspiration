<template>
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
      }

      .museum__about {
        color: #d7d3d0;
        padding: 10px;
        text-align: justify;
      }

      .museum__image {
        height: 85%;
        width: 255%;
        position: relative;
        right: 220px;
      }
    }

    &__section {
      display: none;
    }
  }
</style>