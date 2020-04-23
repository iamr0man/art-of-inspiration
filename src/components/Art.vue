<template>
  <div class="art">
    <div class="art__body">
      <div class="art__header">
        <h1 class="art__number">almond blossom february <span>1890</span></h1>
        <p class="art__additional">Saint-Rémy-de-Provence</p>
      </div>
      <div class="art__details">
        <p class="details__header">highlights</p>
        <p class="details__materials"><span>oil on canvas</span> <span>73,3 cm x 92,3 cm</span></p>
      </div>
      <img class="art__image" src="../assets/photos/art1.jpg" alt="Vincent van Gogh">
      <p class="art__about">The painting was a gift for his brother Theo and sister-in-law Jo, who had just had a baby son, Vincent Willem. In the letter announcing the new arrival, Theo wrote: ‘As we told you, we’ll name him after you, and I’m making the wish that he may be as determined and as courageous as you.’ Unsurprisingly, it was this work that remained closest to the hearts of the Van Gogh family. Vincent Willem went on to found the Van Gogh Museum.</p>
    </div>
    <div class="art__body">
      <div class="art__header">
        <h1 class="art__number">sunflowers january <span>1888</span></h1>
        <p class="art__additional">arles</p>
      </div>
      <div class="art__details">
        <p class="details__header">highlights</p>
        <p class="details__materials"><span>oil on canvas</span> <span>73,3 cm x 92,3 cm</span></p>
      </div>
      <img class="art__image" src="../assets/photos/art2.jpg" alt="Vincent van Gogh">
      <p class="art__about">Van Gogh’s paintings of Sunflowers are among his most famous. He did them in Arles, in the south of France, in 1888 and 1889. Vincent painted a total of five large canvases with sunflowers in a vase, with three shades of yellow ‘and nothing else’. In this way, he demonstrated that it was possible to create an image with numerous variations of a single colour, without any loss of eloquence.</p>
    </div>
    <div class="art__body">
      <div class="art__header">
        <h1 class="art__number">the bedroom october <span>1899</span></h1>
        <p class="art__additional">Arles</p>
      </div>
      <div class="art__details">
        <p class="details__header">highlights</p>
        <p class="details__materials"><span>oil on canvas</span> <span>72,4 cm x 91,3 cm</span></p>
      </div>
      <img class="art__image" src="../assets/photos/art3.jpg" alt="Vincent van Gogh">
      <p class="art__about">While he was in Arles, Van Gogh made this painting of his bedroom in the Yellow House. He prepared the room himself with simple furniture and with his own work on the wall. The bright colours were meant to express absolute ‘repose’ or ‘sleep’. Research shows that the strongly contrasting colours we see in the work today are the result of discolouration over the years. The walls and doors, for instance, were originally purple rather than blue. The apparently odd angle of the rear wall, meanwhile, is not a mistake on Van Gogh’s part – the corner really was skewed.</p>
    </div>
  </div>   
</template>

<script>
export default {

}
</script>

<style lang="scss">
  .art {
    width: 100vw;
    background-color:#1e1e1e;
    color: #fff;

    &__body {
      width: 80%;
      border-right: 2px solid #d7d3d0;
      display: flex;
      flex-direction: column;
      text-align: end;

      &:last-child {
        color: #000;
        background-color: #fff;
        .art__header {
          .art__additional {
            color: #000;
          }
        }
      }

      .art__header {
        display: flex;
        flex-direction: column;

        .art__number {
          font-size: 39px;
          text-transform: uppercase;
          span {
            font-family: 'Armin-Grotesk', sans-serif;
            text-shadow: -1px 0 #000, 0 1px #000, 1px 0 #000, 0 -1px #fff;
          }
        }
        .art__additional {
          font-size: 12px;
          color: #dbd7d3;
        }
      }
    }

    .art__details {
      order: 1;
      text-align: center;
      font-size: 12px;
      
      .details__materials {
        display: flex;
        flex-direction: column;
        margin-top: 10px;
        font-family: 'Armin-Grotesk', sans-serif;
      }
    }

    .art__image {
      width: 125%;
    }

    .art__about {
      font-size: 12px;
      order: 2;
      padding: 20px 0;
    }
  }

  @media screen and (min-width: 1440px) {
    .art {
      &__body{
        width: 89%; 
        padding: 100px;
        flex-direction: row;
        text-align: right;
        flex-wrap: wrap;
        .art__header{
          width: 47%;
          .art__number {
            font-size: 73px;
          } 
        }

        &:nth-child(2n) {
          .art__header {
            order: 2;
          }

          .art__details {
            order: 1;  
            border-left: none; 
            border-right: 2px solid #d7d3d0;          
          }

          .art__about {
            order: 4;
            margin: 0 auto;
            text-align: right;
          }

          .art__image {
            order: 3;
          }
        }

        .art__details {
          order: 0;
          padding: 100px;
          border-left: 2px solid #d7d3d0;
        }
        .art__about {
          font-size: 19px;
          text-align: left;
          width: 50%;
        }
      }
    }
  }
</style>