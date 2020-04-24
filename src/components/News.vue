<template>
  <div class="news">
    <div class="news__aside">
      <div class="news__top">
        <h1 class="news__number">03</h1>
        <canvas ref="canvas" width="400" height="700"></canvas>
      </div>
    </div>
    <div class="news__photo">
      <transition name="fade">
        <img v-show="!loaded" class="news__image" src="../assets/photos/news03.jpeg" alt="">
      </transition>
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
import Ball from '../plugins/ball.js'
export default {
  data(){
    return {
      loaded: true
    }
  },
  methods: {
    initCanvas(){
      var canvas = this.$refs.canvas,
          context = canvas.getContext('2d'),
          balls = [],
          numBalls = 20,
          bounce = -1,
          spring = 0.1;

      for (var ball, i = 0; i < numBalls; i++) {
        ball = new Ball(Math.random() * 30 + 20, Math.random() * 0xffffff);
        ball.x = Math.random() * canvas.width / 2;
        ball.y = Math.random() * canvas.height / 2;
        ball.vx = Math.random() * 6 - 3;
        ball.vy = Math.random() * 6 - 3;
        balls.push(ball);
      }

      function checkCollision (ballA, i) {
        var ballB, dx, dy, dist, min_dist;
        for (var j = i + 1; j < numBalls; j++) {
          ballB = balls[j];
          dx = ballB.x - ballA.x;
          dy = ballB.y - ballA.y;
          dist = Math.sqrt(dx * dx + dy * dy);
          min_dist = ballA.radius + ballB.radius;

          if (dist < min_dist) {
          debugger
            var tx = ballA.x + dx / dist * min_dist,
                ty = ballA.y + dy / dist * min_dist,
                ax = (tx - ballB.x) * spring,
                ay = (ty - ballB.y) * spring;
            ballA.vx -= ax;
            ballA.vy -= ay;
            ballB.vx += ax;
            ballB.vy += ay;
          }
        }
      }

      function move (ball) {
        ball.x += ball.vx;
        ball.y += ball.vy;
        if (ball.x + ball.radius > canvas.width) {
          ball.x = canvas.width - ball.radius;
          ball.vx *= bounce;
        } else if (ball.x - ball.radius < 0) {
          ball.x = ball.radius;
          ball.vx *= bounce;
        }
        if (ball.y + ball.radius > canvas.height) {
          ball.y = canvas.height - ball.radius;
          ball.vy *= bounce;
        } else if (ball.y - ball.radius < 0) {
          ball.y = ball.radius;
          ball.vy *= bounce;
        }
      }

      function draw (ball) {
        ball.draw(context);
      }

      (function drawFrame () {
        window.requestAnimationFrame(drawFrame, canvas);
        context.clearRect(0, 0, canvas.width, canvas.height);

        balls.forEach(checkCollision);
        balls.forEach(move);
        balls.forEach(draw);
      }());
    }
  },
  mounted(){
    this.loaded = false;
    // create bouncing balls;
    this.initCanvas();
  }
}
</script>

<style lang="scss">
  .news {
    width: 100vw;
    background-color:#fef6f0;
    display: flex;
    flex-direction: column;

    .fade-enter-active {
      transition: all .6s ease-in-out;
      transition-delay: 2s;
    }

    .fade-enter-to {
      opacity: 1;
      transform: scale(1);
      transform: translateY(-40px)
    }

    .fade-enter {
      opacity: 0;
      transform: scale(0.3);
      transform: translateY(0)
    }

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

  @media screen and (min-width: 1440px) {
    .news {
      flex-direction: row;
      padding: 20px;
      position: relative;

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
        right: 577px;
      }

      &__photo {
        .news__image {
          width: 124%;
          margin-top: -77px;
        }
      }

      &__aside {
        order: 3;
        flex-direction: row;
        border-right: none;

        .news__top {
          flex-direction: column;
        }
      }

      &__main {
        justify-content: space-evenly;
        border-right: none;
        .news__header{
          font-size: 94px;
        }
        .news__about {
          padding: 70px;
        }
      }
    }
  }
</style>