<template>
  <div class="juices-item">
    <img class="juices-item__img" :src="juices_data.img" alt="img" />
    <div class="juices-item__title">{{ juices_data.title }}, 1 литр</div>
    <div class="juices-item__price">{{ juices_data.price }}</div>
    <button @click="addToCart" class="juices-item__btn">В корзину</button>
  </div>
</template>

<script>
export default {
  data() {
    return {};
  },
  props: {
    juices_data: {
      type: Object,
      default() {
        return {};
      },
    },
  },
  methods: {
    addToCart() {
      this.$emit("addToCart", this.juices_data);
    },
  },
};
</script>

<style lang="scss" scoped>
.juices-item {
  max-width: 235px;
  height: 372px;

  border: 0.2px solid silver;
  border-radius: 5px;

  &__img {
    max-width: 221px;
  }
  &__title {
    font-size: 20px;
    font-weight: normal;
    margin-left: 7px;

    padding-bottom: 25px;
  }
  &__price {
    font-size: 30px;
    font-weight: 600;
    margin-left: 7px;

    padding: 5px 0;
  }
  &__btn {
    width: 221px;
    height: 40px;

    margin: 7px;

    color: #ffff;
    background-color: #1f7d63;
    border: none;
    border-radius: 5px;
    font-size: 17px;
    cursor: pointer;
  }
}
</style>