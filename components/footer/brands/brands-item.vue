<template>
  <div class="brands-item">
    <img class="brands-item__item" :src="brands_data.img" alt="" />
  </div>
</template>

<script>
export default {
  data() {
    return {};
  },
  props: {
    brands_data: {
      type: Object,
      default() {
        return {};
      },
    },
  },
  methods: {},
};
</script>

<style lang="scss" scoped>
.brands-item {
  width: 100%;
  display: grid;
  grid-template-columns: 1fr 1fr 1fr 1fr 1fr 1fr;
  &__item {
    height: 210px;
    width: 210px;
  }
}
</style>