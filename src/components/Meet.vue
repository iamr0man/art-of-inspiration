<template>
  <div class="meet">
    <div class="meet__article">
      <h2 class="meet__header">Meet Vincent</h2>
      <div class="meet__between"></div>
      <h2 class="meet__number">02</h2>
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
    background-color: #1e1e1e;
    display: flex;
    flex-direction: column;
    color: #fff;

    &__article {
      width: 80%;
      border-right: 2px solid #d7d3d0;
      display: flex;
      justify-content: flex-start;
      align-items: baseline;

      .meet__header{
        font-size: 55px;
      }

      .meet__between {
        display: none;
      }

      .meet__number {
        color: #1e1e1e;
        text-shadow: -1px 0 #fff, 0 1px #fff, 1px 0 #fff, 0 -1px #fff;
        font-family: 'Armin-Grotesk', sans-serif;
        font-size: 60px;
      }
    }
  }
</style>