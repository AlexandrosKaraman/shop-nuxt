<template>
  <div class="catalog">
    <p class="catalog__title">Новое поступление</p>
    <div class="catalog__btns">
      <button @click="prevSlide" class="catalog__btn">
        <img
          src="https://www.flaticon.com/svg/vstatic/svg/271/271220.svg?token=exp=1618726603~hmac=403bfef8a824a24002063ccffab525bb"
          alt="arrowLeft"
        />
      </button>
      <button @click="nextSlide" class="catalog__btn">
        <img
          src="https://www.flaticon.com/svg/vstatic/svg/271/271228.svg?token=exp=1618726603~hmac=921205688c3ce274e7fb7c15a53f799c"
          alt="arrowRight"
        />
      </button>
    </div>
    <div
      class="catalog__list"
      :style="{ 'margin-left': '-' + 20 * currentSlideIndex + '%' }"
    >
      <catalog-item
        class="catalog__carousel"
        v-for="product in products"
        :key="product.article"
        :product_data="product"
        @addToCart="addToCart"
      />
    </div>
  </div>
</template>

<script>
import catalogItem from "./catalog-item";
import { mapActions, mapGetters } from "vuex";

export default {
  data() {
    return {
      products: [
        {
          img:
            "https://static-sl.insales.ru/r/XYhJ9USxHI8/fit/440/0/ce/1/plain/images/products/1/5000/379442056/large_%D0%9F%D0%B5%D1%80%D1%81%D0%B8%D0%BA.jpg@webp",
          title: "Персик",
          oldPrice: "110 руб",
          price: "96 руб",
          article: "F1",
          available: true,
          quantity: 1,
        },
        {
          img:
            "https://static-sl.insales.ru/r/zij7-XyPx9I/fit/440/0/ce/1/plain/images/products/1/3971/379449219/large_%D0%91%D0%B0%D0%BA%D0%BB%D0%B0%D0%B6%D0%B0%D0%BD.jpg@webp",
          title: "Баклажан",
          oldPrice: "105 руб",
          price: "82 руб",
          article: "F2",
          available: true,
          quantity: 1,
        },
        {
          img:
            "https://static-sl.insales.ru/r/OhtYntwQrDA/fit/440/0/ce/1/plain/images/products/1/3146/379440202/large_Авокадо.jpg",
          title: "Авокадо",
          oldPrice: "135 руб",
          price: "59 руб",
          article: "F3",
          available: true,
          quantity: 1,
        },
        {
          img:
            "https://static-sl.insales.ru/r/m8RgIbQ3zdA/fit/440/0/ce/1/plain/images/products/1/3554/379440610/large_Ананас.jpg",
          title: "Ананас",
          oldPrice: "187 руб",
          price: "146 руб",
          article: "F4",
          available: true,
          quantity: 1,
        },
        {
          img:
            "https://static-sl.insales.ru/r/imoHnKKHDBM/fit/440/0/ce/1/plain/images/products/1/3787/379440843/large_Гранат.jpg",
          title: "Гранат",
          oldPrice: "320 руб",
          price: "290 руб",
          article: "F5",
          available: true,
          quantity: 1,
        },
        {
          img:
            "https://static-sl.insales.ru/r/PsLxvrkHGu8/fit/440/0/ce/1/plain/images/products/1/4165/379441221/large_Грейпфрут.jpg",
          title: "Грейпфрукт",
          oldPrice: "190 руб",
          price: "140 руб",
          article: "F6",
          available: true,
          quantity: 1,
        },
        {
          img:
            "https://static-sl.insales.ru/r/EnDVWiEA0b8/fit/440/0/ce/1/plain/images/products/1/4563/379441619/large_Груша_дюшес.jpg",
          title: "Груша",
          oldPrice: "115 руб",
          price: "89 руб",
          article: "F7",
          available: true,
          quantity: 1,
        },
        {
          img:
            "https://static-sl.insales.ru/r/mvkG9Soyq60/fit/440/0/ce/1/plain/images/products/1/4981/379450229/large_%D0%9E%D0%B3%D1%83%D1%80%D1%86%D1%8B__1_%D0%BA%D0%B3.jpg@webp",
          title: "Огурцы",
          oldPrice: "118 руб",
          price: "100 руб",
          article: "F8",
          available: true,
          quantity: 1,
        },
        {
          img:
            "https://static-sl.insales.ru/r/lbrdrpEJH7U/fit/440/0/ce/1/plain/images/products/1/5145/379450393/large_%D0%9F%D0%BE%D0%BC%D0%B8%D0%B4%D0%BE%D1%80%D1%8B__1_%D0%BA%D0%B3.jpg@webp",
          title: "Помидоры",
          oldPrice: "102 руб",
          price: "86 руб",
          article: "F9",
          available: true,
          quantity: 1,
        },
        {
          img:
            "https://static-sl.insales.ru/r/iEb2T1DJ3NQ/fit/440/0/ce/1/plain/images/products/1/4052/379457492/large_%D0%9B%D0%B8%D1%81%D1%82%D1%8C%D1%8F_%D1%81%D0%B0%D0%BB%D0%B0%D1%82%D0%B0__100_%D0%B3.jpg@webp",
          title: "Листья салата",
          oldPrice: "115 руб",
          price: "89 руб",
          article: "F10",
          available: true,
          quantity: 1,
        },
      ],
      currentSlideIndex: 0,
    };
  },
  components: {
    catalogItem,
  },
  // computed: { ...mapGetters(["products"]) },

  methods: {
    ...mapActions(
      ["ADD_TO_CART"]
      // ["GET_PRODUCTS_FROM_API"]
    ),
    addToCart(data) {
      this.ADD_TO_CART(data);
    },

    prevSlide() {
      if (this.currentSlideIndex > 0) {
        this.currentSlideIndex--;
      }
    },
    nextSlide() {
      if (this.currentSlideIndex >= 5) {
        this.currentSlideIndex = 0;
      } else {
        this.currentSlideIndex++;
      }
    },

    mounted() {
      // this.GET_PRODUCTS_FROM_API();
    },
  },
};
</script>

<style lang="scss" scoped>
.catalog {
  max-width: 1400px;
  overflow: hidden;

  &__title {
    font-size: 40px;
    font-weight: 600;
  }
  &__list {
    display: flex;
    column-gap: 45px;
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