<template>
  <div class="navbar">
    <div class="menu">
      <nav class="menu__navbar">
        <nuxt-link class="menu__link" to="/catalog">Каталог</nuxt-link>
        <nuxt-link class="menu__link" to="/about">О нас</nuxt-link>
        <nuxt-link class="menu__link" to="/contacts">Контакты</nuxt-link>
        <nuxt-link class="menu__link" to="/shipping">Доставка</nuxt-link>
        <nuxt-link class="menu__link" to="/payment">Оплата</nuxt-link>
        <nuxt-link class="menu__link" to="/account">Кабинет</nuxt-link>
        <nuxt-link class="menu__link" to="/blog">Блог</nuxt-link>
      </nav>
      <div class="menu__info">
        <p>Доставка с 8:00 до 23:00</p>
        <p>+7(800)800-80-80</p>
        <nuxt-link to="#">ES</nuxt-link>
        <nuxt-link to="#">EN</nuxt-link>
        <nuxt-link to="#">RU</nuxt-link>
      </div>
    </div>
    <div class="wrapper">
      <nuxt-link class="wrapper__icon" to="/"
        ><img
          src="https://static-sl.insales.ru/files/1/1171/14550163/original/markom_logo.svg"
          alt="logo"
      /></nuxt-link>
      <button class="wrapper__btn">
        <img
          class="wrapper__icons"
          src="https://www.iconsdb.com/icons/preview/white/arrow-24-xxl.png"
          alt="bars"
        />
        Каталог
      </button>

      <input class="wrapper__input" type="text" placeholder="Поиск" />
      <button class="wrapper__btn">
        <img
          class="wrapper__icons"
          src="https://www.iconsdb.com/icons/preview/white/search-13-xxl.png"
          alt="find"
        />
      </button>

      <img
        class="wrapper__icons"
        src="https://img.icons8.com/ios/2x/user.png"
        alt=""
      />
      <img
        class="wrapper__icons"
        src="https://image.flaticon.com/icons/png/128/1230/1230217.png"
        alt=""
      />
      <img
        class="wrapper__icons"
        src="https://image.flaticon.com/icons/png/128/879/879764.png"
        alt=""
      />
      <p class="wrapper__money">0 руб</p>
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style lang="scss" scoped>
.navbar {
  max-width: 1920px;
  .menu {
    display: grid;
    grid-template-columns: 900px 550px;
    align-content: center;
    justify-content: center;
    background-color: aliceblue;

    width: 100%;
    height: 40px;

    &__navbar {
      display: grid;
      grid-template-columns: repeat(8, 80px);
      justify-items: center;
      align-items: center;
    }
    &__link {
      text-decoration: none;
      color: #000;
    }
    &__link:hover {
      opacity: 0.6;
    }
    &__info {
      display: grid;
      grid-template-columns: 178px 130px 21px 21px 21px;
      justify-items: center;
      align-items: center;
    }
  }
}
.wrapper {
  display: grid;
  grid-template-columns: 250px 160px 547px 70px 56px 56px 50px 50px;
  align-items: center;
  justify-items: center;

  &__btn {
    height: 50px;
    color: white;
    background-color: #1f7d63;
    border-radius: 5px;
    border: none;
    cursor: pointer;

    display: grid;
    grid-template-columns: 35% 50%;
    align-items: center;
  }
  &__input {
    width: 546px;
    height: 40px;

    border-radius: 5px;
  }
  &__icons {
    width: 32px;
  }
  &__icons:first-child {
    width: 20px;
  }
}
</style>