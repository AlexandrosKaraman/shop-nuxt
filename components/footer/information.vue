<template>
  <div class="wrapper">
    <div class="information">
      <div class="information__item">
        <div class="information__title">О магазине Марком</div>
        <a class="information__content" href="#">Адресса магазинов</a>
        <a class="information__content" href="#">Акции и скидки</a>
        <a class="information__content" href="#">Юридическим лицам</a>
        <a class="information__content" href="#">Как заказать</a>
        <a class="information__content" href="#">Обмен и возврат</a>
      </div>
      <div class="information__item">
        <div class="information__title">Покупателям</div>
        <a class="information__content" href="#">Личный кабинет</a>
        <a class="information__content" href="#">Мои заказы</a>
        <a class="information__content" href="#">Вопросы и ответы</a>
        <a class="information__content" href="#">Политика возврата</a>
      </div>

      <div class="information__item">
        <div class="information__title">Информация</div>
        <a class="information__content" href="#"
          >Политика конфиденциальности и оферта</a
        >
        <a class="information__content" href="#">Пользовательское соглашение</a>
      </div>
      <img
        class="information__img"
        src="https://static-sl.insales.ru/files/1/1172/14550164/original/markom_logo_bw.svg"
        alt=""
      />
    </div>
    <div class="social">
      <div class="social__title">Мы в соц. сетях</div>
      <div class="social__group">
        <img
          class="social__icon"
          src="https://static-sl.insales.ru/files/1/1310/14550302/original/dz.svg"
          alt="icon"
        />
        <img
          class="social__icon"
          src="https://static-sl.insales.ru/files/1/1306/14550298/original/fb.svg"
          alt="icon"
        />
        <img
          class="social__icon"
          src="https://static-sl.insales.ru/files/1/1309/14550301/original/twitter.svg"
          alt="icon"
        />
        <img
          class="social__icon"
          src="https://static-sl.insales.ru/files/1/1307/14550299/original/vk.svg"
          alt="icon"
        />
        <img
          class="social__icon"
          src="https://static-sl.insales.ru/files/1/1303/14550295/original/yt.svg"
          alt="icon"
        />
        <img
          class="social__icon"
          src="https://static-sl.insales.ru/files/1/1308/14550300/original/insta.svg"
          alt="icon"
        />
        <img
          class="social__icon"
          src="https://static-sl.insales.ru/files/1/1304/14550296/original/telegram.svg"
          alt="icon"
        />
      </div>
      <div class="social__tel">+7(800) 800-80-80</div>
      <label for="">справочная служба</label>
      <div class="social__tel">+7(800) 800-80-80</div>
      <label for="">справочная служба</label>
      <div class="social__pay">
        <img
          class="social__img"
          src="https://static-sl.insales.ru/files/1/1311/14550303/original/Group.svg"
          alt="imgPay"
        />
        <img
          class="social__img"
          src="https://static-sl.insales.ru/files/1/1305/14550297/original/Visa.svg"
          alt="imgPay"
        />
        <img
          class="social__img"
          src="https://static-sl.insales.ru/files/1/1312/14550304/original/mir-logo_1.svg"
          alt="imgPay"
        />
      </div>
    </div>
  </div>
</template>

<script>
export default {};
</script>



<style lang="scss" scoped>
.wrapper {
  display: grid;
  max-width: 1408px;
  grid-template-columns: 6fr 2fr;
  background-color: rgb(238, 239, 240);

  margin-top: 60px;
}
.information {
  display: grid;
  grid-template-columns: 185px 140px 284px;
  grid-template-rows: min-content;
  max-width: 1408px;
  height: 392px;

  &__item {
    display: grid;
    row-gap: 20px;
    padding-top: 20px;
  }
  &__item:nth-child(1) {
    display: grid;
    grid-template-rows: repeat(6, 20px);
  }
  &__item:nth-child(2) {
    display: grid;
    grid-template-rows: repeat(5, 20px);
  }
  &__item:nth-child(3) {
    display: grid;
    grid-template-rows: repeat(3, 20px);
  }

  &__title {
    font-size: 18px;
    font-weight: 600;
  }
  &__content {
    text-decoration: none;
    color: black;
  }
  &__content:hover {
    color: rgb(193, 241, 144);
  }
  &__img {
    padding-top: 30px;
  }
}

.social {
  display: grid;
  padding-top: 20px;
  &__title {
    font-size: 18px;
    font-weight: 600;
  }
  &__tel {
    font-size: 18px;
    font-weight: 600;
  }
  label {
    padding-bottom: 20px;
  }
}
@media (max-width: 767px) {
  .wrapper {
    display: grid;
    max-width: 1408px;
    grid-template-columns: 1fr;
    background-color: #eeeff0;
    margin-top: 60px;
  }
}
</style>