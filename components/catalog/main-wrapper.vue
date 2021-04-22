<template>
  <div>
    <div class="main-wrapper">
      <catalog />
    </div>
  </div>
</template>

<script>
import catalog from "./catalog";

export default {
  data() {
    return {};
  },
  components: {
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