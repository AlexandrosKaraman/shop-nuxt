<template>
  <div class="cart-item">
    <img class="cart-item__image" :src="cart_item_data.img" alt="" />
    <div class="cart-item__info">
      <div class="new-item__title">{{ cart_item_data.title }}, 1 кг</div>
      <div class="new-item__price">{{ cart_item_data.price }}</div>
      <div class="new-item__article">{{ cart_item_data.article }}</div>
    </div>
    <div class="cart-item__quantity">{{ cart_item_data.quantity }}</div>
    <button @click="deleteFromCart">Delete</button>
  </div>
</template>

<script>
export default {
  props: {
    cart_item_data: {
      type: Object,
      default() {
        return {};
      },
    },
  },
  methods: {
    deleteFromCart() {
      this.$emit("deleteFromCart");
    },
  },
};
</script>

<style lang="scss" scoped>
.cart-item {
  display: flex;
  flex-wrap: nowrap;
  justify-content: space-between;
  align-items: center;

  &__image {
    max-width: 250px;
  }
}
</style>