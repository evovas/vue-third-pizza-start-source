<template>
  <header class="header">
    <div class="header__logo">
      <a href="#" class="logo">
        <img
          src="@/assets/img/logo.svg"
          alt="V!U!E! Pizza logo"
          width="90"
          height="40"
        />
      </a>
    </div>
    <div class="header__cart">
      <a href="#">0 ₽</a>
    </div>
    <div class="header__user">
      <a href="#" class="header__login"><span>Войти</span></a>
    </div>
  </header>
</template>

<script setup></script>

<style scoped lang="scss">
@import "@/assets/scss/ds-system/ds";
.header {
  position: relative;
  z-index: 2;

  display: flex;

  padding: 0 2.12%;

  background-color: $green-500;
  box-shadow: $shadow-light;

  &__logo {
    padding-top: 10px;
    padding-bottom: 10px;
  }

  &__cart {
    margin-right: 10px;
    margin-left: auto;

    a {
      @include b-s16-h19;

      display: block;

      padding-top: 21px;
      padding-right: 15px;
      padding-bottom: 21px;
      padding-left: 58px;

      transition: 0.3s;

      color: $white;
      background-color: $green-500;
      background-image: url("@/assets/img/cart.svg");
      background-repeat: no-repeat;
      background-position: 20px center;
      background-size: 29px 27px;

      &:hover:not(:active) {
        background-color: $green-400;
      }

      &:active {
        background-color: $green-600;
      }

      &:focus {
        opacity: 0.5;
      }
    }
  }

  &__user {
    display: flex;
    align-items: center;

    a {
      display: block;

      padding-top: 14px;
      padding-right: 20px;
      padding-bottom: 14px;
      padding-left: 20px;

      transition: 0.3s;

      background-color: $green-500;

      &:hover:not(:active) {
        background-color: $green-400;
      }

      &:active {
        background-color: $green-600;
      }

      &:focus {
        opacity: 0.5;
      }
    }

    img {
      display: inline-block;

      width: 32px;
      height: 32px;
      margin-right: 8px;

      vertical-align: middle;

      border-radius: 50%;
    }

    span {
      @include r-s14-h16;

      display: inline-block;

      vertical-align: middle;

      color: $white;
    }
  }
  &__logout::before,
  &__login::after {
    display: inline-block;

    width: 32px;
    height: 32px;
    margin-left: 8px;

    content: "";
    vertical-align: middle;
    background-size: auto 50%;
  }

  &__logout {
    &::before {
      background: url("@/assets/img/login.svg") no-repeat center;
    }
  }

  &__login {
    &::after {
      background: url("@/assets/img/login.svg") no-repeat center;
    }
  }
}
</style>
