<template>
  <div>
    <h1>Наши плюсы</h1>

    <div class="qualities">
      <div class="qualities__item">
        <img
          class="qualities__img"
          src="https://static-sl.insales.ru/files/1/3619/14863907/original/plus__1__e21acc6b89a08c337af6fa920e1fe42b.svg"
          alt="img"
        />
        <div class="qualities__title">Широкий ассортимент</div>
        <div class="qualities__content">
          Мы закупаем фрукты и овощи по всему миру – от Эквадора до Китая. Более
          400 сортов овощей и фруктов представлены на наших прилавках.
        </div>
      </div>

      <div class="qualities__item">
        <img
          class="qualities__img"
          src="https://static-sl.insales.ru/files/1/3618/14863906/original/plus__2__cd0e61cab5af76850cc3a312d39f9f20.svg"
          alt="img"
        />
        <div class="qualities__title">Всегда свежие</div>
        <div class="qualities__content">
          Фрукты и овощи перевозятся в машинах-рефрижераторах с разными режимами
          температуры. Мы знаем, сколько градусов внутри каждого плода!
        </div>
      </div>

      <div class="qualities__item">
        <img
          class="qualities__img"
          src="https://static-sl.insales.ru/files/1/3617/14863905/original/plus__3_.svg"
          alt="img"
        />
        <div class="qualities__title">Контроль качества</div>
        <div class="qualities__content">
          Мы контролируем качество – от поставщика до полки. Для хранения мы
          используем самое современное оборудование.
        </div>
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

.qualities {
  width: 100%;
  display: grid;
  grid-template-columns: 3fr 3fr 3fr;

  &__item {
    display: grid;
    grid-template-rows: 102px 36px 144px;

    justify-items: center;
    align-items: center;

    width: 448px;
    height: 314px;
  }
  &__title {
    font-size: 30px;
    font-weight: 600;
  }
  &__content {
    text-align: center;
    font-size: 24px;
  }
}
</style>