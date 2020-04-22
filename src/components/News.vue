<template>
  <div class="news">
    <div class="news__aside">
      <div class="news__top">
        <h1 class="news__number">03</h1>
      </div>
    </div>
    <div class="news__photo">
      <img class="news__image" src="../assets/photos/news03.jpeg" alt="">
    </div>
    <div class="news__main">
      <h2 class="news__header">news</h2>
      <div class="news__about">
        <p class="news__paragraph">Are you a journalist or blogger who wants to visit the museum? Please request a press visit. Some 75 portraits produced by artists of each other in the second half of the 19th century and the early 20th century. Key themes include identity and image-bulding. In the Picture unites major names and new faces.</p>
        <p class="news__paragraph">In addition to portraits by Vincent van Gogh, the exhibition features works by artists including Edvard Munch, Gustave Courbet, Francis Bacon and Helene Schjerfbeck.</p>
      </div>
    </div>
  </div>   
</template>

<script>
export default {

}
</script>

<style lang="scss">
  .news {
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
      .news__top {
        display: flex;
        justify-content: flex-start;
        align-items: baseline;
        .news__number {
          text-shadow: -1px 0 #000, 0 1px #000, 1px 0 #000, 0 -1px #fff;
          color: #fef6f0;
          font-family: 'Armin-Grotesk', sans-serif;
          font-size: 90px;
          margin: 20px 0;
        }

      }
      .news__image {
        display: none;
      }
    }

    &__photo {
      .news__image {
        width: 100%;
      }
    }

    &__main {
      width: 80%;
      display: flex;
      flex-direction: column;
      justify-content: space-between;
      border-right: 2px solid #d7d3d0;
      
      .news__header {
        display: flex;
        flex-direction: column;
        align-items: flex-end;
        text-transform: uppercase;
        font-size: 44px;
      }

      .news__about {
        display: flex;
        flex-direction: column;
        padding: 10px;
        color: #d7d3d0;
        text-align: justify;

        .news__paragraph {
          margin-top: 20px;
        }
      }

    }
  }
</style>