<template>
  <div class="page">
    <Navbar />
    <Nuxt />
  </div>
</template>

<script>
import Navbar from "../components/Navbar";

export default {
  component: {
    Navbar,
  },
};
</script>

<style>
/* .page {
  display: grid;
  justify-content: center;
  margin: 0 auto;
} */
</style>
