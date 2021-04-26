<template>
  <div class="nuts-item">
    <img class="nuts-item__img" :src="nuts_data.img" alt="img" />
    <div class="nuts-item__title">{{ nuts_data.title }}, {{ scale }}</div>
    <div class="nuts-item__price">{{ nuts_data.price }}</div>
    <button @click="addToCart" class="nuts-item__btn">В корзину</button>
  </div>
</template>

<script>
export default {
  data() {
    return {
      scale: " кг",
    };
  },
  props: {
    nuts_data: {
      type: Object,
      default() {
        return {};
      },
    },
  },
  methods: {
    addToCart() {
      this.$emit("addToCart", this.nuts_data);
    },
  },
};
</script>

<style lang="scss" scoped>
.nuts-item {
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
  &__btn:active {
    opacity: 0.8;
    box-shadow: 0 1px 0 #00823f;
    bottom: -4px;
  }
}
</style>