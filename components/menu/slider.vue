<template>
  <div class="slider">
    <div class="gallery">
      <no-ssr>
        <flickity class="slider-wrap" ref="flickity" :options="flickityOptions">
          <div class="carousel-cell">1</div>
          <div class="carousel-cell">2</div>
          <div class="carousel-cell">3</div>
          <div class="carousel-cell">4</div>
          <div class="carousel-cell">5</div>
        </flickity>
      </no-ssr>
    </div>
    <div class="container menu_select"></div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      flickityOptions: {
        initialIndex: 0,
        prevNextButtons: true,
        pageDots: false,
        wrapAround: true
      }
    };
  }
};
</script>

<style lang="scss" scoped>
.slider {
  width: 100%;
  height: 390px;
  background: #000;

  .gallery {
    width: 100%;
    height: 390px;
    background-color: #fff;

    .slider-wrap {
      width: 100%;

      .carousel-cell {
        width: 66%;
        height: 390px;
        margin-right: 10px;
        background: #8c8;
        border-radius: 5px;
        counter-increment: carousel-cell;
      }
    }
  }
}
</style>
