<template>
  <div>
    <h1>Корзина</h1>
    <div class="v-cart">
      <cart-item
        v-for="(item, index) in cart_data"
        :key="item.article"
        :cart_item_data="item"
        @deleteFromCart="deleteFromCart(index)"
      />
    </div>
  </div>
</template>

<script>
import { mapActions } from "vuex";
import cartItem from "./cart-item";
export default {
  components: { cartItem },
  props: {
    cart_data: {
      type: Array,
      default() {
        return [];
      },
    },
  },
  methods: {
    ...mapActions(["DELETE_FROM_CART"]),
    deleteFromCart(index) {
      this.DELETE_FROM_CART(index);
    },
  },
};
</script>

<style lang="scss" scoped>
.v-cart {
  width: 1400px;
  height: 600px;
}
</style>