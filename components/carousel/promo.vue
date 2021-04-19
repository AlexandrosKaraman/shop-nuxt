<template>
  <div class="promo">
    <carousel>
      <carousel-slide
        v-for="slide in slides"
        :key="slide"
        class="carousel-slider"
      >
        <img :src="slide" :alt="slide" />
      </carousel-slide>
    </carousel>
  </div>
</template>

<script>
import Carousel from "./carousel.vue";
import CarouselSlide from "./carouselSlide.vue";

export default {
  data() {
    return {
      slides: [
        "https://static-sl.insales.ru/r/nlEYOkOZekE/fit/1408/0/ce/1/plain/files/1/2110/14641214/original/slider.jpg@webp",
        "https://static-sl.insales.ru/r/nlEYOkOZekE/fit/1408/0/ce/1/plain/files/1/2110/14641214/original/slider.jpg@webp",
      ],
    };
  },

  components: {
    Carousel: Carousel,
    CarouselSlide: CarouselSlide,
  },
};
</script>

<style>
.carousel {
  position: relative;
  overflow: hidden;
  width: 1450px;
  height: 470px;
  z-index: 10;
}
.btn {
  padding: 5px 10px;
  background-color: rgba(0, 0, 0, 0.5);
  border: 1px solid transparent;
  margin: 5px 10px;
  color: #fff;
  height: 50px;
  width: 50px;
  position: absolute;
  margin-top: -25px;
  z-index: 2;
}
.btn:hover {
  cursor: pointer;
}
.btn:focus {
  outline: none;
}
.btn-next {
  top: 50%;
  right: 0;
}
.btn-prev {
  top: 50%;
  left: 0;
}
.carousel-slider {
  position: absolute;
  top: 0;
  left: 0;
  bottom: 0;
  right: 0;
}
.carousel-slider img {
  width: 100%;
  height: 100%;
}
</style>