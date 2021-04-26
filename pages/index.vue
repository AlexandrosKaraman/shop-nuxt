<template>
  <div class="container">
    <div>
      <promo />
    </div>
    <div>
      <main-wrapper />
    </div>
    <div>
      <group />
    </div>
    <div>
      <desserts />
    </div>
    <div>
      <juices />
    </div>
    <div>
      <nuts />
    </div>
    <div>
      <qualities />
    </div>
    <div>
      <brands />
    </div>
    <div>
      <shares />
    </div>
    <div>
      <feedback />
    </div>
    <div>
      <formInput />
    </div>
    <div>
      <information />
    </div>
  </div>
</template>

<script>
import MainWrapper from "~/components/catalog/main-wrapper.vue";
import desserts from "~/components/Desserts.vue";
import Brands from "~/components/footer/brands/brands.vue";
import Feedback from "~/components/footer/feedback.vue";
import information from "~/components/footer/information.vue";
import Qualities from "~/components/footer/qualities.vue";
import Shares from "~/components/footer/shares.vue";
import FormInput from "~/components/forms/form-input.vue";
import juices from "~/components/juices/juices.vue";
import nuts from "~/components/nuts/nuts.vue";
import promo from "../components/carousel/promo.vue";
import group from "../components/Group.vue";

export default {
  components: {
    promo,
    MainWrapper,
    group,
    desserts,
    juices,
    nuts,
    Qualities,
    Brands,
    Shares,
    Feedback,
    information,
    FormInput,
  },
};
</script>


<style>
.container {
  max-width: 1404px;

  margin: 0 auto;
}
@media (max-width: 1408px) {
  .container {
    max-width: 970px;
  }
}
@media (max-width: 992px) {
  .container {
    max-width: 750px;
  }
}
@media (max-width: 767px) {
  .container {
    max-width: none;
  }
}
</style>
