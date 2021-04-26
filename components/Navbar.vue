<template>
  <div class="navbar">
    <div class="burger">
      <div>
        <svg
          xmlns="http://www.w3.org/2000/svg"
          height="24px"
          viewBox="0 0 24 24"
          width="24px"
          fill="#000000"
        >
          <path d="M0 0h24v24H0V0z" fill="none" />
          <path d="M3 18h18v-2H3v2zm0-5h18v-2H3v2zm0-7v2h18V6H3z" />
        </svg>
      </div>

      <nuxt-link class="wrapper__icon" to="/"
        ><img
          src="https://static-sl.insales.ru/files/1/1171/14550163/original/markom_logo.svg"
          alt="logo"
      /></nuxt-link>

      <div>
        <nuxt-link class="wrapper__cart" to="/blog">
          <img
            class="wrapper__icons"
            src="https://image.flaticon.com/icons/png/128/879/879764.png"
            alt=""
          />
        </nuxt-link>
      </div>
    </div>
    <div class="menu">
      <nav class="menu__links">
        <nuxt-link class="menu__link" to="/catalog">Каталог</nuxt-link>
        <nuxt-link class="menu__link" to="/about">О нас</nuxt-link>
        <nuxt-link class="menu__link" to="/contacts">Контакты</nuxt-link>
        <nuxt-link class="menu__link" to="/shipping">Доставка</nuxt-link>
        <nuxt-link class="menu__link" to="/payment">Оплата</nuxt-link>
        <nuxt-link class="menu__link" to="/account">Кабинет</nuxt-link>
        <nuxt-link class="menu__link" to="/blog">Корзина</nuxt-link>
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
        <svg
          class="wrapper__icon"
          xmlns="http://www.w3.org/2000/svg"
          height="24px"
          viewBox="0 0 24 24"
          width="24px"
          fill="#FFFFFF"
        >
          <path d="M0 0h24v24H0V0z" fill="none" />
          <path d="M3 19h18v-6H3v6zm0-8h18V9H3v2zm0-6v2h18V5H3z" />
        </svg>
        Каталог
      </button>

      <input class="wrapper__input" type="text" placeholder="Поиск" />
      <button class="wrapper__btn">
        <svg
          class="wrapper__icons"
          xmlns="http://www.w3.org/2000/svg"
          height="24px"
          viewBox="0 0 24 24"
          width="24px"
          fill="#FFFFFF"
        >
          <path d="M0 0h24v24H0z" fill="none" />
          <path
            d="M15.5 14h-.79l-.28-.27C15.41 12.59 16 11.11 16 9.5 16 5.91 13.09 3 9.5 3S3 5.91 3 9.5 5.91 16 9.5 16c1.61 0 3.09-.59 4.23-1.57l.27.28v.79l5 4.99L20.49 19l-4.99-5zm-6 0C7.01 14 5 11.99 5 9.5S7.01 5 9.5 5 14 7.01 14 9.5 11.99 14 9.5 14z"
          />
        </svg>
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
      <nuxt-link class="wrapper__cart" to="/blog">
        <img
          class="wrapper__icons"
          src="https://image.flaticon.com/icons/png/128/879/879764.png"
          alt=""
        />
      </nuxt-link>
      <p class="wrapper__money">0 руб</p>
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style lang="scss" scoped>
.burger {
  display: none;
}

.navbar {
  max-width: 1408px;
  width: 100%;
  margin: 0 auto;

  @media (max-width: 767px) {
    .burger {
      max-width: 767px;
      height: 90px;
      position: relative;
      display: grid;
      grid-template-columns: 1fr 1fr 1fr;
      margin: 0 auto;
      justify-items: center;
      align-items: center;
    }
    .menu,
    .navbar,
    .wrapper {
      display: none;
    }
  }

  // @media (max-width: 767px) {
  //   &__burger {
  //     display: block;
  //     position: relative;
  //     width: 30px;
  //     height: 20px;
  //   }
  //   &__burger span {
  //     position: absolute;
  //     background-color: #ffff;
  //     left: 0;
  //     width: 100%;
  //     height: 2px;
  //     top: 9px;
  //   }
  //   &__burger:before,
  //   &__burger:after {
  //     content: "";
  //     background-color: #ffff;
  //     position: absolute;
  //     width: 100%;
  //     height: 2px;
  //   }
  //   &__burger:before {
  //     top: 0;
  //   }
  //   &__burger:after {
  //     bottom: 0;
  //   }
  // }
}
.menu {
  display: grid;
  grid-template-columns: 6fr 3fr;
  align-content: center;
  justify-content: center;
  background-color: aliceblue;

  width: 100%;
  height: 40px;

  &__links {
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
  @media (max-width: 992px) {
    &__info {
      display: none;
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
  &__icon:hover {
    opacity: 0.8;
  }
  &__icon:active {
    transform: scale(1.1);
  }
  &__icons {
    width: 32px;
  }
  &__icons:first-child {
    width: 20px;
  }
  &__cart:hover {
    margin: 0 auto;
    background-color: rgb(204, 204, 204);
    color: white;

    transform: scale(1.6);
  }
}
</style>