<template>
  <div>
    <div>
      <div class="blog" v-if="!CART.length">
        <h3 class="blog__title">Корзина пуста...</h3>
        <nuxt-link class="blog__link" to="/">Вернуться на главную</nuxt-link>
      </div>
      <v-cart v-if="CART.length" :cart_data="CART" />
    </div>
  </div>
</template>

<script>
import { mapGetters } from "vuex";
import vCart from "../components/catalog/cart/v-cart";

export default {
  components: {
    vCart,
  },

  computed: mapGetters(["CART"]),
};
</script>

<style lang="scss" scoped>
.blog {
  &__title {
    text-align: center;
    margin: 150px;
    font-size: 40px;
  }
  &__link {
    display: flex;
    justify-content: center;
    padding: 100px;
    cursor: pointer;
    font-size: 30px;
    text-decoration: none;
    color: blueviolet;
  }
  &__link:hover {
    transform: scale(1.4);
    color: red;
  }
}
</style>