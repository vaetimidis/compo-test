<template>
  <header class="header">
    <div class="header__top">
      <div class="logo">
        <img class="logo__img" src="/public/logo.svg" alt="logo">
      </div>
      <button class="button button--menu button--blue">
        <span>Меню</span>
      </button>
      <div class="search">
        <form class="form">
          <div class="input">
            <input id="" aria-label="Поиск" class="input__field" inputmode="text" name="" placeholder="Поиск по сайту" type="text">
            <div class="search__buttons">
              <button type="button" class="search__button cross" />
              <button type="submit" class="search__button find" />
            </div>
          </div>
        </form>
      </div>
      <div class="header-buttons">
        <div class="header-buttons__item">
          <a href="" class="header-buttons__link">
            <img class="header-buttons__img" src="/public/notification.svg" alt="">
          </a>
        </div>
        <div class="header-buttons__item">
          <a href="" class="header-buttons__link favorite">
            <img class="header-buttons__img" src="/public/favorite.svg" alt="">
          </a>
        </div>
      </div>
      <button class="button button--lightblue button--cart">
        <span class="button__text button__text--cart">144 155₽</span>
      </button>
      <div class="info">
        <div class="avatar">
          <img class="avatar__img" src="/public/avatar.svg" alt="avatar">
        </div>
        <span class="name">Ермаков Е.</span>
        <button class="info__menu" />
      </div>
    </div>
    <div class="header__bottom">
      <div class="navigation navigation--left">
        <a class="navigation__item">Мои заказы</a>
        <a class="navigation__item">Сотрудники</a>
        <a class="navigation__item">Шаблоны заказов</a>
        <a class="navigation__item">Обращения</a>
      </div>
      <div class="navigation navigation--right">
        <a class="button button--lightblue button--manager">
          Ваш менеджер
        </a>
        <a class="button button--white button--discount">
          Акции
        </a>
        <a class="navigation__item navigation__item--blue">
          Блог
        </a>
      </div>
    </div>
  </header>
</template>

<style lang="scss" scoped>
.header {
    display: flex;
    flex-direction: column;
    height: 136px;

    &__top {
      display: flex;
      flex-direction: row;
      height: 80px;
      padding: 16px 24px;
      gap: 24px;
      border-bottom: 1px solid #E1E5EB;

    }

    &__bottom {
      display: flex;
      flex-direction: row;
      height: 56px;
      padding: 12px 24px;
      gap: 16px;
      border-bottom: 1px solid #E1E5EB;
    }
  }

.logo {
  display: flex;
  align-items: center;
  justify-content: center;
  height: 48px;

  &__img {
    width: 144px;
    height: 28px;
  }
}

.button {
  display: flex;
  flex-direction: row;
  align-items: center;
  justify-content: center;

  border-radius: 8px;
  gap: 12px;
  padding: 12px 24px;

  color: #fff;

  &__text{
  line-height: 16px;

  &--cart {
    color: #1551E5;
    font-size: 14px;
    font-weight: 700;
  }
}

  &--blue {
    background-color: #1551E5;
    height: 48px;
  }

  &--lightblue {
    background-color: #F2F6FF;
  }

  &--menu::before {
    content: url('/public/menu.svg');
    width: 24px;
    height: 24px;
  }

  &--cart {
    height: 48px;

    &::before {
      content: url('/public/cart.svg');
      width: 24px;
      height: 24px;
    }
  }

  &--manager {
    font-weight: 400;
    font-size: 14px;
    line-height: 16px;
    color: #1551E5;
    gap: 8px;
    padding: 8px 12px;
    height: 32px;
    border-radius: 4px;

    &::before {
      content: url('/public/chat.svg');
      width: 16px;
      height: 16px
    }
  }

  &--white {
    background-color: #fff;
  }

  &--discount {
    font-weight: 400;
    font-size: 14px;
    line-height: 16px;
    color: #1551E5;
    display: flex;
    flex-direction: row;
    align-items: center;
    justify-content: center;
    gap: 16px;

    &::before {
      content: url('/public/discount.svg');
      height: 16px;
      width: 16px;
    }
  }
}

.search {
  display: flex;
  flex-direction: row;
  align-items: center;
  height: 48px;

  &__buttons {
    display: flex;
    flex-direction: row;
    gap: 12px;
  }

  &__button {
    display: flex;
    align-items: center;
    justify-content: center;
  }

  .cross::before {
    content: url('/public/cross.svg');
    height: 24px;
    width: 24px;
  }

  .find::before {
    content: url('/public/search.svg');
    height: 24px;
    width: 24px;
  }

}

.input {
  width: 100%;
  height: 48px;

  display: flex;
  flex-direction: row;
  align-items: center;
  justify-content: center;

  border: 1px solid #E1E5EB;
  border-radius: 8px;
  padding: 8px 12px 8px 16px;

  &__field {
    background-color: transparent;
    border: none;
  }
}

.header-buttons {
  display: flex;
  flex-direction: row;
  align-items: center;
  height: 48px;

  &__item {
    padding: 0 24px;
  }

  &__link {
    display: flex;
    align-items: center;
    justify-content: center;
  }

  &__img {
    width: 32px;
    height: 32px;
  }
}

.info {
  display: flex;
  flex-direction: row;
  align-items: center;
  justify-content: center;
  gap: 16px;
  height: 48px;

  &__menu {
    display: flex;
    align-items: center;
    justify-content: center;

    &::before {
      content: url('/public/arrow-down.svg');
      height: 24px;
      width: 24px
    }
  }
}

.avatar {
  display: flex;
  align-items: center;
  justify-content: center;

  &__img {
    width: 32px;
    height: 32px;
  }
}

.navigation {
  display: flex;
  flex-direction: row;
  align-items: center;
  gap: 24px;

  &--right {
    margin-left: auto;
    color: #1551E5;
  }

  &__item {
    font-weight: 400;
    font-size: 14px;
    line-height: 16px;
    color: #071435;

    &--blue {
      color: #1551E5;
    }
  }
}
</style>
