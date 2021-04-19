<template>
  <div class="main-wrapper">
    <catalog />
  </div>
</template>

<script>
import catalog from "./catalog";

export default {
  data() {
    return {};
  },
  component: {
    catalog,
  },
};
</script>

<style lang="scss" scoped>
.main-wrapper {
  max-width: 1400px;
  width: 100%;
  margin: 0 auto;
}
</style>