<template>
  <header class="header">
    <div class="header__top">
      <div class="logo logo--copy">
        <img alt="" height="" src="/public/logo.svg" width="">
      </div>
      <button class="button button--blue button--menu">
        Меню
      </button>
      <form class="search">
        <div class="search__input">
          <input id="form_text" aria-label="Поиск" inputmode="text" name="form_text" placeholder="Название запроса" type="text">
          <button aria-label="Отмена" type="button" class="search__button search__button--cross" />
          <button aria-label="Поиск" type="submit" class="search__button search__button--find" />
        </div>
      </form>
      <a class="button button--icon button--notification" href="javascript:void(0);" title="" />
      <div class="header__line" />
      <a class="button button--icon button--favorite" href="javascript:void(0);" title="" />
      <a class="button button--lightblue button--cart" href="javascript:void(0);" title="">
        144 155₽
      </a>
      <button class="header__info">
        <div class="header__info-avatar">
          <img alt="" height="" src="/public/Avatar.png" width="">
        </div>
        Ермаков Е.
      </button>
    </div>
    <div class="header__bottom">
      <nav class="navigation">
        <a class="navigation__link" href="javascript:void(0);" title="">Мои заказы</a>
        <a class="navigation__link" href="javascript:void(0);" title="">Сотрудники</a>
        <a class="navigation__link" href="javascript:void(0);" title="">Шаблоны заказов</a>
        <a class="navigation__link" href="javascript:void(0);" title="">Обращения</a>
      </nav>
      <div class="header__links">
        <a class="header__link header__link--manager" href="javascript:void(0);" title="">Ваш менеджер</a>
        <a class="header__link header__link--special" href="javascript:void(0);" title="">Акции</a>
        <a class="header__link" href="javascript:void(0);" title="">Блог</a>
      </div>
    </div>
  </header>
</template>

<style lang="scss" scoped>
button,
input {
  outline: none;
}

.header {
  box-shadow: 0 4px 8px -16px #F0F3FC;

  &__top {
    align-items: center;
    border-bottom: 1px solid #E1E5EB;
    display: flex;
    gap: 24px;
    padding: 16px 24px;
  }

  &__bottom {
    align-items: center;
    border-bottom: 1px solid #E1E5EB;
    display: flex;
    gap: 16px;
    padding: 12px 24px;
  }

  &__line {
    background: #E2E4F0;
    height: 48px;
    width: 1px;
  }

  &__links {
    align-items: center;
    display: flex;
    gap: 24px;
  }

  &__link {
    align-items: center;
    display: flex;
    color: #1551E5;
    font-size: 14px;
    font-weight: 400;
    gap: 8px;
    line-height: 16px;
    text-decoration: none;
    transition: opacity .3s;

    @media (hover: none), (pointer: coarse) {
      &:active {
        opacity: .7;
      }
    }

    @media not all and (pointer: coarse) {
      &:hover,
      &:active {
        opacity: .7;
      }
    }

    &--manager {
      background: #F2F6FF;
      border-radius: 4px;
      padding: 8px 12px;

      &:before {
        content: url('/public/chat.svg');
        width: 16px;
        height: 16px
      }
    }

    &--special {
      &:before {
        content: url('/public/discount.svg');
        height: 16px;
        width: 16px;
      }
    }
  }

  &__info {
    align-items: center;
    color: #071435;
    display: flex;
    font-size: 14px;
    font-weight: 400;
    gap: 16px;
    line-height: 16px;
    text-decoration: none;
    transition: opacity .3s;

    @media (hover: none), (pointer: coarse) {
      &:active {
        opacity: .7;
      }
    }

    @media not all and (pointer: coarse) {
      &:hover,
      &:active {
        opacity: .7;
      }
    }

    &:after {
      content: url('/public/arrow-down.svg');
      height: 24px;
      width: 24px
    }
  }

  &__info-avatar {
    border-radius: 8px;
    height: 32px;
    overflow: hidden;
    width: 32px;

    img {
      height: 32px;
      object-fit: contain;
      width: 32px;
    }
  }
}

.search {
  background: #FFFFFF;
  border: 1px solid #E1E5EB;
  border-radius: 8px;
  display: flex;
  flex-grow: 1;
  padding: 6px 10px 6px 14px;

  &__input {
    align-items: center;
    display: flex;
    font-size: 14px;
    font-weight: 400;
    gap: 12px;
    line-height: 16px;
    width: 100%;

    input {
      flex-grow: 1;

      &[placeholder] {
          text-overflow: ellipsis;
      }

      &::-webkit-input-placeholder {
        color: #050D23;
      }

      &:-moz-placeholder {
        color: #050D23;
      }

      &::-moz-placeholder {
        color: #050D23;
      }

      &:-ms-input-placeholder {
        color: #050D23;
      }
    }
  }

  &__button {
    display: flex;
    height: 24px;
    transition: opacity .3s;
    width: 24px;

    @media (hover: none), (pointer: coarse) {
      &:active {
        opacity: .7;
      }
    }

    @media not all and (pointer: coarse) {
      &:hover,
      &:active {
        opacity: .7;
      }
    }

    &:before {
      height: 24px;
      width: 24px;
    }

    &--cross {
      &:before {
        content: url('/public/cross.svg');
      }
    }

    &--find {
      &:before {
        content: url('/public/search.svg');
      }
    }
  }
}

.navigation {
  align-items: center;
  display: flex;
  flex-grow: 1;
  gap: 24px;

  &__link {
    color: #071435;
    font-size: 14px;
    font-weight: 400;
    line-height: 16px;
    text-decoration: none;
    transition: opacity .3s;

    @media (hover: none), (pointer: coarse) {
      &:active {
        opacity: .7;
      }
    }

    @media not all and (pointer: coarse) {
      &:hover,
      &:active {
        opacity: .7;
      }
    }
  }
}
</style>
