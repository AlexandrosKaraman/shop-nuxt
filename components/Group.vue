<template>
  <div class="group">
    <div class="big">
      <div class="big__item">
        <img
          class="big__img"
          src="https://static-sl.insales.ru/r/m-0zp_CP79Q/fit/700/700/ce/1/plain/files/1/6822/14351014/original/Фото__1_.jpg"
          alt="img"
        />
        <div class="big__title">Торты, десерты, сладкая выпечка</div>
      </div>

      <div class="big__item">
        <img
          class="big__img"
          src="https://static-sl.insales.ru/r/CAZ604l3KmE/fit/700/700/ce/1/plain/files/1/6845/14351037/original/Фото__2_.jpg"
          alt="img"
        />
        <div class="big__title">Рыба, икра, морекродукты</div>
      </div>
    </div>

    <div class="little">
      <div class="little__item">
        <img
          class="little__img"
          src="https://static-sl.insales.ru/r/VgcYMCg0nIU/fit/700/700/ce/1/plain/files/1/6949/14351141/original/Фото__5_.jpg"
          alt="img"
        />
        <div class="little__title">Овощи</div>
      </div>

      <div class="little__item">
        <img
          class="little__img"
          src="https://static-sl.insales.ru/r/p3c-EkRiM8E/fit/700/700/ce/1/plain/files/1/6962/14351154/original/Фото__6_.jpg"
          alt="img"
        />
        <div class="little__title">Ягоды</div>
      </div>

      <div class="little__item">
        <img
          class="little__img"
          src="https://static-sl.insales.ru/r/Clx3D1pCJ9Q/fit/700/700/ce/1/plain/files/1/6988/14351180/original/Фото__7_.jpg"
          alt="img"
        />
        <div class="little__title">Мясо</div>
      </div>
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style lang="scss" scoped>
.group {
  max-width: 1408px;
  width: 100%;

  .big {
    display: grid;
    grid-template-columns: 692px 692px;
    gap: 50px;
    padding: 30px 0;

    &__item {
      height: 416px;
      border: 0.5px solid silver;
      border-radius: 5px;
    }

    &__title {
      padding: 20px;
      font-size: 20px;
    }

    &__img {
      width: 692px;
    }
  }

  .little {
    display: grid;
    grid-template-columns: 454px 454px 454px;
    column-gap: 36px;

    &__item {
      border: 0.5px solid silver;
      border-radius: 5px;

      border-radius: 5px;
    }
    &__img {
      width: 454px;
    }
    &__title {
      padding: 20px;
      font-size: 20px;
    }
  }
  @media (max-width: 767px) {
    .big {
      max-width: 500px;
      grid-template-columns: 1fr;
      margin: 0 auto;
    }
    .big img {
      width: 500px;
      height: 340px;
    }
    .little {
      max-width: 455px;
      grid-template-columns: 1fr;
      margin: 0 auto;
      justify-content: space-between;
      gap: 25px;
    }
  }
}
</style>