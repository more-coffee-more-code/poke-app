<template>
  <div class="carousel">
    <p class="carousel__label">Swipe to see your Pokemon</p>
    <flickity ref="flickity" :options="flickityOptions">
      <div class="carousel-cell">
        <figure class="carousel-cell__image-wrapper">
          <img src="../assets/images/pikachu.png" alt="" class="carousel-cell__iamge">
        </figure>
      </div>
      <div class="carousel-cell">
        <figure class="carousel-cell__image-wrapper">
          <img src="../assets/images/plant-guy.png" alt="" class="carousel-cell__iamge">
        </figure>
      </div>
      <div class="carousel-cell">
        <figure class="carousel-cell__image-wrapper">
          <img src="../assets/images/bulb-guy.png" alt="" class="carousel-cell__iamge">
        </figure>
      </div>
  </flickity>
  </div>
</template>
<script>
import Flickity from 'vue-flickity';

export default {
  name: 'Carousel',
  data() {
    return {
      flickityOptions: {
        initialIndex: 1,
        prevNextButtons: false,
        pageDots: true,
        wrapAround: false,
      }
    }
  },
  components: {
    Flickity
  }
}
</script>
<style lang="scss" scoped>
@import '../assets/css/global-styles';

.carousel {
  margin: 30px auto;
  width: 90%; 

  &__label {
    color: $white;
  }

  &-cell {
    height: 300px;
    width: 100%;
    margin: 20px 0 -30px;

    &__image-wrapper {
    margin: 20px 25px 10px;
    border: solid 3px $poke-yellow;
    width: 300px;
    margin: 0 auto;
    }
  }
}

.flickity-page-dots {
  margin-top: -30px;
  background: white;
}
</style>