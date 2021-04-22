<template>
  <div>
    <div>
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

<style>
</style>