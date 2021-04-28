<template>
  <div class="new-item">
    <img class="new-item__img" :src="product_data.img" alt="img" />
    <div class="new-item__title">{{ product_data.title }}, 1 кг</div>
    <div class="new-item__old-price">{{ product_data.oldPrice }}</div>
    <div class="new-item__price">{{ product_data.price }}</div>
    <button @click="addToCart" class="new-item__btn">В корзину</button>
  </div>
</template>

<script>
export default {
  data() {
    return {};
  },
  props: {
    product_data: {
      type: Object,
      default() {
        return {};
      },
    },
  },
  methods: {
    addToCart() {
      this.$emit("addToCart", this.product_data);
    },
  },
};
</script>

<style lang="scss" scoped>
.new-item {
  max-width: 235px;
  height: 410px;

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
  &__old-price {
    font-size: 25px;
    text-decoration: line-through;
    padding: 5px 0;
    margin-left: 7px;

    opacity: 0.8;
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