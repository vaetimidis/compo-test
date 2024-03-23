<template>
  <footer class="footer">
    <div class="footer__top">
      <div class="navigation navigation--left">
        <div class="logo">
          <img class="logo__img" src="/public/logo.svg" alt="logo">
        </div>
        <div class="contacts">
          <div class="contacts__item">
            <a class="contacts__link" href="tel:+88008419595" title="8 800 841-95-95">8 800 841-95-95</a>
            <div class="contacts__text">
              Служба поддержки
            </div>
          </div>
          <div class="contacts__item">
            <a class="contacts__link" href="mailto:support@sport.ru" title="support@sport.ru">support@sport.ru</a>
            <div class="contacts__text">
              Служба поддержки
            </div>
          </div>
        </div>
      </div>
      <div class="navigation navigation--right">
        <a href="" class="navigation__link">Вакансии</a>
        <a href="" class="navigation__link">Блог</a>
        <a href="" class="navigation__link">Акции</a>
        <button class="button button--lightblue button--navigation">
          Предложить идею
        </button>
      </div>
    </div>
    <div class="footer__main catalog">
      <div class="catalog__item">
        <div class="menu-header">
          Женщинам
        </div>
        <ul class="menu">
          <li class="menu__item">
            Одежда
          </li>
          <li class="menu__item">
            Обувь
          </li>
          <li class="menu__item">
            Аксессуары
          </li>
          <li class="menu__item">
            Белье
          </li>
          <li class="menu__item">
            Bra fitting
          </li>
        </ul>
      </div>
      <div class="catalog__item">
        <div class="menu-header">
          Мужчинам
        </div>
        <ul class="menu">
          <li class="menu__item">
            Одежда
          </li>
          <li class="menu__item">
            Обувь
          </li>
          <li class="menu__item">
            Аксессуары
          </li>
          <li class="menu__item">
            Белье
          </li>
        </ul>
      </div> <div class="catalog__item">
        <div class="menu-header">
          Детям
        </div>
        <ul class="menu">
          <li class="menu__item">
            Одежда
          </li>
          <li class="menu__item">
            Обувь
          </li>
          <li class="menu__item">
            Аксессуары
          </li>
          <li class="menu__item">
            Белье
          </li>
          <li class="menu__item">
            Игрушки
          </li>
          <li class="menu__item">
            Малыши
          </li>
        </ul>
      </div> <div class="catalog__item">
        <div class="menu-header">
          Виды спорта
        </div>
        <ul class="menu">
          <li class="menu__item">
            Велоспорт
          </li>
          <li class="menu__item">
            Туризм
          </li>
          <li class="menu__item">
            Тренажеры и фитнес
          </li>
          <li class="menu__item">
            Командные виды спорта
          </li>
          <li class="menu__item">
            Самокаты
          </li>
        </ul>
      </div>
    </div>
    <div class="footer__bottom">
      <div class="links">
        <a href="" class="links__item links__item--presentation"><span class="links__text">PDF презентация</span></a>
        <a href="" class="links__item links__item--video"><span class="links__text">Видео инструкция</span></a>
        <a href="" class="links__item links__item--faq"><span class="links__text">FAQ</span></a>
        <a href="" class="links__item links__item--youtube"><span class="links__text">Мы на YouTube</span></a>
        <a href="" class="links__item"><span class="links__text">Политика конфиденциальности</span></a>
        <a href="" class="links__item"><span class="links__text">Лицензионное соглашение</span></a>
      </div>
      <div class="politics">
        <p>Настоящая Политика обработки персональных данных разработана в соответствии с Конституцией Российской Федерации, Трудовым кодексом Российской Федерации, Гражданским кодексом Российской Федерации, Федеральным законом от 27 июля 2006 года 149-ФЗ "Об информации, информационных технологиях и о защите информации",</p>
      </div>
      <div class="copyright">
        <div class="copyright__logo">
          <img class="copyright__img" src="/public/logo-gray.svg" alt="">
        </div>
        <div class="copyright__description">
          Разработка платформы
        </div>
      </div>
    </div>
  </footer>
</template>

<style lang="scss" scoped>
.footer {
  margin-top: 120px;
  display: flex;
  flex-direction: column;
  padding: 0 24px;

  &__top {
    display: flex;
    flex-direction: row;
    align-items: center;
    justify-content: space-between;

    padding: 48px 0;
    border-top: 1px solid #E2E4F0;
  }

  &__main {
    display: flex;
    flex-direction: row;
    align-items: flex-start;
    justify-content: center;
    align-self: flex-start;
    gap: 24px;
    width: 100%;
    padding: 48px 0;
    border-top: 1px solid #E2E4F0;

  }

  &__bottom {
    display: flex;
    flex-direction: column;
    align-items: center;
    gap: 48px;
    padding: 48px 0;
    border-top: 1px solid #E2E4F0;

  }
}

.menu {
    list-style-type: none;
    display: flex;
    flex-direction: column;
    gap: 14px;
    margin: 0;
    padding: 0;

    &__item {
        font-weight: 400;
        font-size: 14px;
        line-height: 16px;
        color: #050D23
    }
}

.logo {
    display: flex;
    align-items: center;
    justify-content: center;

    &__img {
        height: 40px;
    }
}

.menu-header {
    font-weight: 500;
    font-size: 16px;
    line-height: 24px;
    color: #050D23;
}

.catalog {
    display: flex;
    flex-direction: row;

    &__item {
        display: flex;
        flex-direction: column;
        align-items: flex-start;
        width: calc(100% / 4);
        gap: 24px
    }
}

.navigation {
    display: flex;
    flex-direction: row;
    align-items: center;

    &--left {
      padding: 8px;
      gap: 56px;
    }

    &--right {
        gap: 32px
    }

    &__link {
        font-weight: 700;
        font-size: 16px;
        line-height: 20px;
        color: #071435;
        text-decoration: none;
    }
}

.button {
    display: flex;
    flex-direction: row;
    align-items: center;

    &--lightblue {
        background-color: #F2F6FF;
    }

    &--navigation {
        border-radius: 8px;
        padding: 12px 24px;
        gap: 12px;
        height: 48px;
        color: #1551E5;

        font-weight: 500;
        font-size: 14px;
        line-height: 16px;

    }
}

.contacts {
    display: flex;
    flex-direction: row;
    align-items: center;
    gap: 48px;

    &__item {
        display: flex;
        flex-direction: column;
        align-items: center;
        gap: 16px;
    }

    &__text {
        font-weight: 400;
        font-size: 12px;
        line-height: 16px;
        color: #77829E;
    }

    &__link {
        font-weight: 700;
        font-size: 16px;
        line-height: 20px;
        color: #050D23;
        text-decoration: none
    }
}

.links {
    display: flex;
    flex-direction: row;
    align-items: center;
    gap: 28px;

    &__item {
      display: flex;
      align-items: center;
      justify-content: center;
      text-decoration: none;
      gap: 8px;

      &--presentation::before {
        content: url('/public/file.svg');
        height: 16px;
        width: 16px;
      }

      &--video::before {
        content: url('/public/camera.svg');
        height: 16px;
        width: 16px;
      }

      &--faq::before {
        content: url('/public/exclamation.svg');
        height: 16px;
        width: 16px;
      }

      &--youtube::before {
        content: url('/public/youtube.svg');
        height: 16px;
        width: 16px;
      }
    }

    &__text {
        font-weight: 500;
        font-size: 12px;
        line-height: 16px;
        color: #828EAD;
      }
}

.politics {
    font-weight: 400;
    font-size: 12px;
    line-height: 16px;
    text-align: center;
    color: #828EAD;
}

.copyright {
    display: flex;
    flex-direction: row;
    align-items: center;
    gap: 24px;

    &__logo {
      display: flex;
      justify-content: center;
      align-items: center;
    }

    &__img {
      height: 24px;
    }

    &__description {
        font-weight: 700;
        font-size: 14px;
        line-height: 16px;
        color: #8F9BB3;
    }
}
</style>
