<template>
  <div class="carousel" @keydown="checkSlide($event)" tabindex="0">
    <slot></slot>
    <button @click.prevent="next" class="btn btn-next">
      <img
        src="https://www.iconsdb.com/icons/preview/white/arrow-24-xxl.png"
        alt=""
      />
    </button>
    <!-- <p class="carousel__title">Премиум продукты высокого качества</p> -->
    <button @click.prevent="prev" class="btn btn-prev">
      <img
        src="https://www.iconsdb.com/icons/preview/white/arrow-88-xxl.png"
        alt=""
      />
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