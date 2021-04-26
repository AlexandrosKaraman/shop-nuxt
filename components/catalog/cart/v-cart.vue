<template>
  <div>
    <h1>Корзина</h1>
    <div class="v-cart">
      <cart-item
        v-for="(item, index) in cart_data"
        :key="item.article"
        :cart_item_data="item"
        @deleteFromCart="deleteFromCart(index)"
        @increment="increment(index)"
        @decrement="decrement(index)"
      />
    </div>
    <div class="v-cart__total">
      <p class="v-cart__name">Total:</p>
      <p>{{ cartTotalCost }} рублей</p>
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
    ...mapActions([
      "DELETE_FROM_CART",
      "INCREMENT_ITEM_CART",
      "DECREMENT_ITEM_CART",
    ]),
    increment(index) {
      this.INCREMENT_ITEM_CART(index);
    },
    decrement(index) {
      this.DECREMENT_ITEM_CART(index);
    },
    deleteFromCart(index) {
      this.DELETE_FROM_CART(index);
    },
  },
  computed: {
    cartTotalCost() {
      let result = [];
      if (this.cart_data.length) {
        for (let i of this.cart_data) {
          result.push(i.price * i.quantity);
        }
        result = result.reduce(function (sum, el) {
          return sum + el;
        });
        return result;
      } else {
        return 0;
      }
    },
  },
};
</script>

<style lang="scss" scoped>
h1 {
  text-align: center;
}
.v-cart {
  max-width: 1400px;
  height: 600px;
  margin: auto;
  &__total {
    height: 110px;
    position: fixed;
    bottom: 0;
    left: 0;
    right: 0;
    padding: 50px;
    display: flex;
    justify-content: center;
    background: #2e8b17;
    color: white;
    font-size: 30px;
  }
  &__name {
    margin-right: 20px;
  }
}
</style>