<template>
  <v-layout class="rounded rounded-md">
    <div class="header">
      <div class="header-main">
        <div class="header-main__logo">
          <img src="/public/logo.svg" alt="logo">
        </div>
        <button class="header-main__menu">
          <v-icon icon="mdi-format-list-bulleted" color="#FFF" />
          <span>Меню</span>
        </button>
        <div class="header-search">
          <v-text-field
            class="header-search"
            append-inner-icon="mdi-magnify"
            dense
            label="Название запроса"
            variant="solo"
            hide-details
            single-line
            clearable
          />
        </div>
        <div class="header-main__icons">
          <a href="/" class="header-main__icon-wrapper">
            <img class="header-main__icon" src="/public/notification.svg" alt="notification">
          </a>
          <a href="/" class="header-main__icon-wrapper">
            <img class="header-main__icon" src="/public/favorite.svg" alt="favorite">
          </a>
        </div>
        <div class="header-main__cart" />
        <div class="header-main__user" />
      </div>
      <div class="header-submenu" />
    </div>
  </v-layout>
</template>

<style lang="scss">
.header {
  position: fixed !important;
  top: 0;
  width: 100%;
  height: 136px;
  z-index: 1000;
}

.header-main {
  display: flex;
  flex-direction: row;
  align-items: center;
  justify-content: space-between;

  height: 80px;
  padding: 16px 24px;

  border-bottom: 1px solid gray;

  &__logo {
    display: flex !important;
    flex: none !important;
    width: 144px;
    height: 28px;
  }

  &__menu {
    display: flex;
    align-items: center;
    justify-content: space-between;

    background-color: blue;
    color: #FFF;

    height: 48px;
    border-radius: 8px;
    padding: 12px 24px;
  }

  &__icons {
    display: flex;
    align-items: center;
    height: 48px;
    width: 112px;
  }

  &__icon-wrapper {
    display: flex;
    align-items: center;
    position: relative;
    padding: 0 24px;
  }

  &__icon {
    width: 32px;
    height: 32px
  }

  &__icon-wrapper::after {
    content: '';
    position: absolute;
    top: 50%;
    right: 0;
    width: 1px;
    height: 48px;
    background-color: #E2E4F0;
    transform: translateY(-50%);
  }

  &__icon-wrapper:last-child::after {
    content: none;
  }

}

.header-search {
  width: 731px !important;
}
</style>
