<template>
  <div>
    <h1>Акции</h1>
    <div class="shares">
      <div class="shares__item">
        <img
          class="shares__img"
          src="https://static-sl.insales.ru/r/M7doH9VEMF0/fit/390/390/ce/1/plain/images/articles/1/5974/1161046/large_Фото__9_.jpg"
          alt=""
        />
        <div class="shares__title">
          Отборные фрукты и овощи, с привлекательной ценой
        </div>
        <div class="shares__date">10.11.2020</div>
      </div>

      <div class="shares__item">
        <img
          class="shares__img"
          src="https://static-sl.insales.ru/r/037mwZIFSmw/fit/390/390/ce/1/plain/images/articles/1/5973/1161045/large_Новость.jpg"
          alt=""
        />
        <div class="shares__title">Дни испанской кухни</div>
        <div class="shares__date">10.11.2020</div>
      </div>

      <div class="shares__item">
        <img
          class="shares__img"
          src="https://static-sl.insales.ru/r/CIlpH8NKMLE/fit/390/390/ce/1/plain/images/articles/1/5972/1161044/large_Фото__8_.jpg"
          alt=""
        />
        <div class="shares__title">Скидка на зерновой кофе</div>
        <div class="shares__date">20.07.2017</div>
      </div>

      <div class="shares__item">
        <img
          class="shares__img"
          src="https://static-sl.insales.ru/r/DyOZaKI3Eow/fit/390/390/ce/1/plain/images/articles/1/5971/1161043/large_Фото.jpg"
          alt=""
        />
        <div class="shares__title">Скидка на всю выпечку 40% после 19:00</div>
        <div class="shares__date">31.01.2016</div>
      </div>
    </div>
  </div>
</template>

<script>
export default {};
</script>



<style lang="scss" scoped>
h1 {
  margin: 70px 0px 40px 0px;
}
.shares {
  display: grid;
  grid-template-columns: 2fr 2fr 2fr 2fr;
  &__img {
    width: 328px;
    height: 328px;

    border: none;
    border-radius: 10px;
  }
  &__title {
    max-width: 328px;
    font-size: 24px;
    font-weight: 600;
  }
}
</style>