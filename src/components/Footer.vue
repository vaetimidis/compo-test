<!-- eslint-disable vue/valid-v-for -->
<script setup lang="ts">
import { ref } from 'vue'

const links = ref([
  {
    title: 'Женщинам',
    items: [{
      name: 'Одежда',
      id: 1,
    }, {
      name: 'Обувь',
      id: 2,
    }, {
      name: 'Аксессуары',
      id: 3,
    }, {
      name: 'Белье',
      id: 4,
    }, {
      name: 'Bra fitting',
      id: 5,
    }],
    id: 1,
  },
  {
    title: 'Мужчинам',
    items: [{
      name: 'Одежда',
      id: 1,
    }, {
      name: 'Обувь',
      id: 2,
    }, {
      name: 'Аксессуары',
      id: 3,
    }, {
      name: 'Белье',
      id: 4,
    }],
    id: 2,
  },
  {
    title: 'Детям',
    items: [{
      name: 'Одежда',
      id: 1,
    }, {
      name: 'Обувь',
      id: 2,
    }, {
      name: 'Аксессуары',
      id: 3,
    }, {
      name: 'Белье',
      id: 4,
    }, {
      name: 'Игрушки',
      id: 5,
    }, {
      name: 'Малыши',
      id: 6,
    }],
    id: 3,
  },
  {
    title: 'Виды спорта',
    items: [{
      name: 'Велоспорт',
      id: 1,
    }, {
      name: 'Туризм',
      id: 2,
    }, {
      name: 'Тренажеры и фитнес',
      id: 3,
    }, {
      name: 'Командные виды спорта',
      id: 4,
    }, {
      name: 'Самокаты',
      id: 5,
    }],
    id: 4,
  },
])
</script>

<template>
  <footer class="footer">
    <div class="footer__line" />
    <div class="footer__top">
      <div class="footer__contacts-cont">
        <a class="logo logo--footer" href="javascript:void(0);" title="">
          <img alt="" class="logo__img" height="" src="/public/logo.svg" width="">
        </a>
        <div class="footer__contacts">
          <div class="footer__contacts-item">
            <a class="footer__contacts-link" href="tel:+88008419595" title="">8 800 841-95-95</a>
            <div class="footer__contacts-text">
              Служба поддержки
            </div>
          </div>
          <div class="footer__contacts-item">
            <a class="footer__contacts-link" href="mailto:support@sport.ru" title="">support@sport.ru</a>
            <div class="footer__contacts-text">
              Служба поддержки
            </div>
          </div>
        </div>
      </div>
      <div class="footer__links">
        <a class="footer__link" href="javascript:void(0);" title="">Вакансии</a>
        <a class="footer__link" href="javascript:void(0);" title="">Блог</a>
        <a class="footer__link" href="javascript:void(0);" title="">Акции</a>
        <button class="button button--lightblue">
          Предложить идею
        </button>
      </div>
    </div>
    <div class="footer__line" />
    <div class="footer__main">
      <div class="menu">
        <div v-for="item in links" :key="item.id" class="menu__group">
          <div class="menu__group-title">
            {{ item.title }}
          </div>
          <div class="menu__list">
            <a v-for="link in item.items" :key="link.id" class="menu__link" href="javascript:void(0);" title="">
              {{ link.name }}
            </a>
          </div>
        </div>
      </div>
    </div>
    <div class="footer__line" />
    <div class="footer__bottom">
      <div class="footer__info">
        <a class="footer__info-link footer__info-link--presentation" href="javascript:void(0);" title="">PDF презентация</a>
        <a class="footer__info-link footer__info-link--video" href="javascript:void(0);" title="">Видео инструкция</a>
        <a class="footer__info-link footer__info-link--faq" href="javascript:void(0);" title="">FAQ</a>
        <a class="footer__info-link footer__info-link--youtube" href="javascript:void(0);" title="">Мы на YouTube</a>
        <a class="footer__info-link" href="javascript:void(0);" title="">Политика конфиденциальности</a>
        <a class="footer__info-link" href="javascript:void(0);" title="">Лицензионное соглашение</a>
      </div>
      <div class="footer__politics">
        Настоящая Политика обработки персональных данных разработана в соответствии с Конституцией Российской Федерации, Трудовым кодексом Российской Федерации, Гражданским кодексом Российской Федерации, Федеральным законом от 27 июля 2006 года 149-ФЗ "Об информации, информационных технологиях и о защите информации",
      </div>
      <div class="footer__copyright">
        <div class="logo--copy">
          <img alt="" height="" src="/public/logo-gray.svg" width="">
        </div>
        Разработка платформы
      </div>
    </div>
  </footer>
</template>

<style lang="scss" scoped>
.footer {
  display: flex;
  flex-direction: column;
  gap: 48px;
  padding: 0 24px;

  &__line {
    background: #E2E4F0;
    height: 1px;
    width: 100%;
  }

  &__top {
    align-items: center;
    display: flex;
  }

  &__contacts-cont {
    align-items: center;
    display: flex;
    gap: 56px;
  }

  &__contacts {
    align-items: center;
    display: flex;
    gap: 48px;
  }

  &__contacts-item {
    display: flex;
    flex-direction: column;
    gap: 16px;
  }

  &__contacts-link {
    color: #050D23;
    font-size: 16px;
    font-weight: 700;
    line-height: 20px;
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

  &__contacts-text {
    color: #77829E;
    font-size: 12px;
    font-weight: 400;
    line-height: 16px;
  }

  &__links {
    align-items: center;
    display: flex;
    gap: 32px;
    margin-left: auto;
  }

  &__link {
    color: #071435;
    font-size: 16px;
    font-weight: 700;
    line-height: 20px;
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

  &__bottom {
    align-items: center;
    display: flex;
    flex-direction: column;
    gap: 40px;
    padding-bottom: 40px;
  }

  &__info {
    align-items: center;
    display: flex;
    gap: 28px;
  }

  &__info-link {
    align-items: center;
    color: #828EAD;
    display: flex;
    font-size: 12px;
    font-weight: 500;
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

    &--presentation {
      &:before {
        content: url('/public/file.svg');
        height: 16px;
        width: 16px;
      }
    }

    &--video {
      &:before {
        content: url('/public/camera.svg');
        height: 16px;
        width: 16px;
      }
    }

    &--faq {
      &:before {
        content: url('/public/exclamation.svg');
        height: 16px;
        width: 16px;
      }
    }

    &--youtube {
      color: #1551E5;

      &:before {
        content: url('/public/youtube.svg');
        height: 16px;
        width: 16px;
      }
    }
  }

  &__politics {
    color: #828EAD;
    font-size: 12px;
    font-weight: 400;
    line-height: 16px;
    text-align: center;
  }

  &__copyright {
    align-items: center;
    color: #8F9BB3;
    display: flex;
    font-size: 14px;
    font-weight: 700;
    line-height: 16px;
    gap: 24px;
  }
}

.menu {
  display: flex;
  gap: 24px;

  &__group {
    display: flex;
    flex-direction: column;
    gap: 24px;
    width: calc(100% / 4 - 24px / 3);
  }

  &__group-title {
    color: #050D23;
    font-size: 16px;
    font-weight: 500;
    line-height: 24px;
  }

  &__list {
    display: flex;
    flex-direction: column;
    gap: 16px;
  }

  &__link {
    color: #050D23;
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

/* убрать */
.logo {
  display: block;
  height: 28px;
  transition: opacity .3s;
  width: 144px;

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

  img {
    height: 100%;
    object-fit: contain;
    width: 100%;
  }

  &--footer {
    height: 40px;
    width: 192px;
  }

  &--copy {
    height: 24px;
    width: 124px;
  }
}
/* убрать */
.button {
  align-items: center;
  border-radius: 8px;
  display: flex;
  font-size: 14px;
  font-weight: 700;
  gap: 12px;
  justify-content: center;
  line-height: 16px;
  padding: 12px 24px;
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

  &--lightblue {
    background: #F2F6FF;
    color: #1551E5;
  }
}
</style>
