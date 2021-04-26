<template>
  <div class="cart-item">
    <img class="cart-item__image" :src="cart_item_data.img" alt="" />
    <div class="cart-item__info">
      <div class="cart-item__title">{{ cart_item_data.title }}</div>
      <div class="cart-item__price">{{ cart_item_data.price }} руб</div>
      <div class="cart-item__buttons">
        <span class="cart-item__btn" @click="decrementItem">-</span>
        <div class="cart-item__quantity">{{ cart_item_data.quantity }} кг</div>
        <span class="cart-item__btn" @click="incrementItem">+</span>
      </div>
    </div>
    <button class="cart-item__close" @click="deleteFromCart">
      <svg
        xmlns="http://www.w3.org/2000/svg"
        height="24px"
        viewBox="0 0 24 24"
        width="24px"
        fill="#000000"
      >
        <path d="M0 0h24v24H0V0z" fill="none" />
        <path
          d="M19 6.41L17.59 5 12 10.59 6.41 5 5 6.41 10.59 12 5 17.59 6.41 19 12 13.41 17.59 19 19 17.59 13.41 12 19 6.41z"
        />
      </svg>
    </button>
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
    decrementItem() {
      this.$emit("decrement");
    },
    incrementItem() {
      this.$emit("increment");
    },
  },
};
</script>

<style lang="scss" scoped>
.cart-item {
  max-width: 983px;
  display: grid;
  grid-template-columns: 240px 400px 400px;

  &__info {
    display: grid;
    grid-template-rows: 50px 50px 50px;
    padding-top: 35px;
    padding-left: 15px;
  }

  &__title {
    font-size: 24px;
    font-weight: 600;
  }
  &__price {
    font-size: 18px;
    color: #1f7d63;
  }

  &__image {
    max-width: 250px;
  }
  &__buttons {
    width: 140px;
    height: 30px;

    display: grid;
    grid-template-columns: 30px 80px 30px;
    justify-items: center;
    align-items: center;
    background-color: #1f7d63;
    color: #ffff;

    border: none;
    border-radius: 10px;
  }
  &__btn {
    font-size: 30px;
    cursor: pointer;
  }
  // &__btn:active {
  //   background-color: #1f7d63;
  // }
  // &__btn:hover {
  //   opacity: 0.7;
  // }
  &__close {
    border: none;
    background-color: #fff;
    cursor: pointer;
    width: 25px;
    height: 25px;
    margin: 35px;
    justify-self: center;
  }
  &__close:hover {
    transform: scale(1.2);
  }
  &__close:active {
    opacity: 0.7;
  }
}
</style>