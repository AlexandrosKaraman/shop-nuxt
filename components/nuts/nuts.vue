<template>
  <div class="nuts">
    <p class="nuts__title">Орехи</p>
    <div class="nuts__list">
      <nuts-item
        v-for="nut in nuts"
        :key="nut.article"
        :nuts_data="nut"
        @addToCart="addToCart"
      />
    </div>
  </div>
</template>

<script>
import { mapActions } from "vuex";
import nutsItem from "./nuts-item";

export default {
  data() {
    return {
      nuts: [
        {
          img:
            "https://static-sl.insales.ru/r/fJXdMGLZML8/fit/440/0/ce/1/plain/images/products/1/7824/379428496/large_Фундук_очищенный.jpg",
          title: "Фундук очищенный",
          price: "1600 руб",
          article: "N1",
          available: true,
          quantity: 1,
        },
        {
          img:
            "https://static-sl.insales.ru/r/nPMdA3qdAlI/fit/440/0/ce/1/plain/images/products/1/6166/379418646/large_Грецкий_орех.jpg",
          title: "Грецкий орех",
          price: "1110 руб",
          article: "N2",
          available: true,
          quantity: 1,
        },
        {
          img:
            "https://static-sl.insales.ru/r/BDJvRonRsyQ/fit/440/0/ce/1/plain/images/products/1/6586/379427258/large_Фисташки_в_скорлупе.jpg",
          title: "Фисташки",
          price: "900 руб",
          article: "N3",
          available: true,
          quantity: 1,
        },
        {
          img:
            "https://static-sl.insales.ru/r/zJ2noREIisw/fit/440/0/ce/1/plain/images/products/1/6841/379419321/large_Кешью.jpg",
          title: "Кешью",
          price: "1128 руб",
          article: "N4",
          available: true,
          quantity: 1,
        },
        {
          img:
            "https://static-sl.insales.ru/r/PM0mpM8FaK8/fit/440/0/ce/1/plain/images/products/1/7379/379419859/large_Миндаль.jpg",
          title: "Миндаль",
          price: "1500 руб",
          article: "N5",
          available: true,
          quantity: 1,
        },
        {
          img:
            "https://static-sl.insales.ru/r/LUSFzg8_fC8/fit/440/0/ce/1/plain/images/products/1/7151/379427823/large_Фундук_в_скорлупе.jpg",
          title: "Фундук в скорлупе",
          price: "1000 руб",
          article: "N6",
          available: true,
          quantity: 1,
        },
      ],
    };
  },
  components: {
    nutsItem,
  },
  methods: {
    ...mapActions(["ADD_TO_CART"]),
    addToCart(data) {
      this.ADD_TO_CART(data);
    },
  },
};
</script>

<style lang="scss" scoped>
.nuts {
  &__title {
    font-size: 40px;
    font-weight: 600;
  }
  &__list {
    display: grid;
    grid-template-columns: 1fr 1fr 1fr 1fr 1fr 1fr;
    grid-template-rows: 2fr;
  }
}
</style>