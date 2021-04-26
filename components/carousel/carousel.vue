<template>
  <div class="carousel" @keydown="checkSlide($event)" tabindex="0">
    <slot></slot>
    <button @click.prevent="next" class="btn btn-next">
      <svg
        xmlns="http://www.w3.org/2000/svg"
        height="24px"
        viewBox="0 0 24 24"
        width="24px"
        fill="#FFFFFF"
      >
        <path d="M0 0h24v24H0z" fill="none" />
        <path d="M10 6L8.59 7.41 13.17 12l-4.58 4.59L10 18l6-6z" />
      </svg>
    </button>
    <!-- <p class="carousel__title">Премиум продукты высокого качества</p> -->
    <button @click.prevent="prev" class="btn btn-prev">
      <svg
        xmlns="http://www.w3.org/2000/svg"
        height="24px"
        viewBox="0 0 24 24"
        width="24px"
        fill="#FFFFFF"
      >
        <path d="M0 0h24v24H0z" fill="none" />
        <path d="M15.41 7.41L14 6l-6 6 6 6 1.41-1.41L10.83 12z" />
      </svg>
    </button>
  </div>
</template>
<script>
export default {
  data() {
    return {
      index: 0,
      slides: [],
      slideDirection: "",
    };
  },
  computed: {
    slidesLength() {
      return this.slides.length;
    },
  },
  mounted() {
    this.slides = this.$children;
    this.slides.map((slide, index) => {
      slide.index = index;
    });
  },
  methods: {
    next() {
      this.index++;
      if (this.index >= this.slidesLength) {
        this.index = 0;
      }
      this.slideDirection = "slide-right";
    },
    prev() {
      this.index--;
      if (this.index < 0) {
        this.index = this.slidesLength - 1;
      }
      this.slideDirection = "slide-left";
    },
    checkSlide(event) {
      if (event.keyCode === 39) {
        this.next();
      } else if (event.keyCode === 37) {
        this.prev();
      } else {
        return;
      }
    },
  },
};
</script>
<style lang="scss" scoped>
*img {
  width: 30px;
  position: relative;
  z-index: 4;
}

.carousel {
  &__title {
    position: relative;
    z-index: 3;
    font-size: 55px;
    font-weight: 600;
    color: #ffff;
    padding-top: 150px;
  }
}
</style>