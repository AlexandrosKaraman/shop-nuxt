<template>
  <div class="desserts">
    <div class="desserts__img">
      <div class="desserts__title">Десерты на заказ</div>
      <div class="desserts__content">
        Сладкие шедевры ручной работы по рецептам нашего шеф-кондитера.
        Индивидуальные десерты, разнообразие <br />начинок, индивидуальный
        подход! Скидки именинникам.
      </div>
      <button class="desserts__btn">Узнать больше</button>
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style lang="scss" scoped>
.desserts {
  width: 100%;
  height: 100%;

  margin: 40px 0;

  &__img {
    height: 318px;
    background-image: url(https://static-sl.insales.ru/r/MjqsHu0tN0g/fit/1408/0/ce/1/plain/files/1/2281/14797033/original/info_2.jpg);
    position: relative;
  }

  &__title {
    font-size: 40px;
    color: #ffff;

    padding: 40px;
  }
  &__content {
    font-size: 25px;
    color: #ffff;
    padding: 0 40px;
  }
  &__btn {
    height: 50px;
    color: white;
    background-color: #1f7d63;
    border-radius: 5px;
    border: none;
    margin: 40px;
  }
}
</style>