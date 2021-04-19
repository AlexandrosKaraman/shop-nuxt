<template>
  <div>
    <div class="brands">
      <p class="brands__title">Бренды</p>
      <div class="brands__btns">
        <button @click="prevBrand" class="brands__btn">
          <img
            src="https://www.flaticon.com/svg/vstatic/svg/271/271220.svg?token=exp=1618726603~hmac=403bfef8a824a24002063ccffab525bb"
            alt="arrowLeft"
          />
        </button>
        <button @click="nextBrand" class="brands__btn">
          <img
            src="https://www.flaticon.com/svg/vstatic/svg/271/271228.svg?token=exp=1618726603~hmac=921205688c3ce274e7fb7c15a53f799c"
            alt="arrowRight"
          />
        </button>
      </div>
      <div
        class="brands__list"
        :style="{ 'margin-left': '-' + 19 * currentBrandArticle + '%' }"
      >
        <brandsItem
          v-for="brand in brands"
          :key="brand.article"
          :brands_data="brand"
        />
      </div>
    </div>
  </div>
</template>

<script>
import brandsItem from "./brands-item";

export default {
  data() {
    return {
      brands: [
        {
          img:
            "https://static-sl.insales.ru/r/UgsrK9VwG9I/fit/500/500/ce/1/plain/files/1/4361/14930185/original/Component.png",
          article: "T1",
          available: true,
        },
        {
          img:
            "https://static-sl.insales.ru/r/PmMBfn2FIw8/fit/500/500/ce/1/plain/files/1/4363/14930187/original/Component-2.png",
          article: "T2",
          available: true,
        },
        {
          img:
            "https://static-sl.insales.ru/r/SeLqG_V0Vv8/fit/500/500/ce/1/plain/files/1/4363/14930187/original/Component-2.png@webp",
          article: "T3",
          available: true,
        },
        {
          img:
            "https://static-sl.insales.ru/r/puhKdHkSJjs/fit/500/500/ce/1/plain/files/1/4357/14930181/original/Component-10.png@webp",
          article: "T4",
          available: true,
        },
        {
          img:
            "https://static-sl.insales.ru/r/gtriESJoraA/fit/500/500/ce/1/plain/files/1/4366/14930190/original/Component-4.png@webp",
          article: "T5",
          available: true,
        },
        {
          img:
            "https://static-sl.insales.ru/r/x9XHttDC2mM/fit/500/500/ce/1/plain/files/1/4360/14930184/original/Component-5.png@webp",
          article: "T6",
          available: true,
        },
        {
          img:
            "https://static-sl.insales.ru/r/puhKdHkSJjs/fit/500/500/ce/1/plain/files/1/4357/14930181/original/Component-10.png@webp",
          article: "T7",
          available: true,
        },
        {
          img:
            "https://static-sl.insales.ru/r/UgsrK9VwG9I/fit/500/500/ce/1/plain/files/1/4361/14930185/original/Component.png",
          article: "T8",
          available: true,
        },
        {
          img:
            "https://static-sl.insales.ru/r/PmMBfn2FIw8/fit/500/500/ce/1/plain/files/1/4363/14930187/original/Component-2.png",
          article: "T9",
          available: true,
        },
        {
          img:
            "https://static-sl.insales.ru/r/8E5w1B05jro/fit/500/500/ce/1/plain/files/1/4365/14930189/original/Component-3.png@webp",
          article: "T10",
          available: true,
        },
      ],
      currentBrandArticle: 0,
    };
  },
  components: {
    brandsItem,
  },
  methods: {
    prevBrand() {
      if (this.currentBrandArticle > 0) {
        this.currentBrandArticle--;
      }
    },
    nextBrand() {
      if (this.currentBrandArticle >= 2) {
        this.currentBrandArticle = 0;
      } else {
        this.currentBrandArticle++;
      }
    },
  },
};
</script>



<style lang="scss" scoped>
.brands {
  max-width: 1400px;
  overflow: hidden;

  &__title {
    font-size: 40px;
    font-weight: 600;
  }
  &__list {
    display: flex;
    column-gap: 30px;
    transition: all ease 0.5s;
  }
  &__btns {
    display: flex;
    justify-content: flex-end;
    padding: 20px;
  }
  &__btn {
    width: 40px;
    height: 40px;
  }
}
</style>