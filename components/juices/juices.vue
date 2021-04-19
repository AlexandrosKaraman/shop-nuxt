<template>
  <div class="juices">
    <p class="juices__title">Вода, соки, напитки</p>
    <div class="juices__list">
      <juices-item
        v-for="juice in juices"
        :key="juice.article"
        :juices_data="juice"
      />
    </div>
  </div>
</template>

<script>
import juicesItem from "./juices-item";

export default {
  data() {
    return {
      juices: [
        {
          img:
            "https://static-sl.insales.ru/r/DT2m2SF6wuQ/fit/440/0/ce/1/plain/images/products/1/2339/380438819/large_Сок_апельсин__1_л.jpg",
          title: "Сок апельсин",
          price: "120 руб",
          article: "T1",
          available: true,
        },
        {
          img:
            "https://static-sl.insales.ru/r/feTRTX4b3CM/fit/440/0/ce/1/plain/images/products/1/2870/380439350/large_Сок_банан__1_л.jpg",
          title: "Сок банан",
          price: "120 руб",
          article: "T2",
          available: true,
        },
        {
          img:
            "https://static-sl.insales.ru/r/SKuVy0ksuFY/fit/440/0/ce/1/plain/images/products/1/3008/380439488/large_Сок_гранат__1_л.jpg",
          title: "Сок гранат",
          price: "140 руб",
          article: "T3",
          available: true,
        },
        {
          img:
            "https://static-sl.insales.ru/r/3QaRcxaCB1U/fit/440/0/ce/1/plain/images/products/1/3105/380439585/large_Сок_грепфрут__1_л.jpg",
          title: "Сок грейпфрут",
          price: "120 руб",
          article: "T4",
          available: true,
        },
        {
          img:
            "https://static-sl.insales.ru/r/YCB81GJHAzQ/fit/440/0/ce/1/plain/images/products/1/3224/380439704/large_Сок_яблоко__1_л.jpg",
          title: "Сок яблоко",
          price: "100 руб",
          article: "T5",
          available: true,
        },
        {
          img:
            "https://static-sl.insales.ru/r/Che0D73ilrE/fit/440/0/ce/1/plain/images/products/1/1706/380438186/large_Сок_ананас__1_л.jpg",
          title: "Сок ананас",
          price: "120 руб",
          article: "T6",
          available: true,
        },
      ],
    };
  },
  components: {
    juicesItem,
  },
};
</script>

<style lang="scss" scoped>
.juices {
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