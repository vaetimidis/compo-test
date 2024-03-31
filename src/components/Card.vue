<script setup lang="ts">
import Breadcrumbs from './Breadcrumbs.vue'

import { Swiper, SwiperSlide, useSwiper } from 'swiper/vue'

import 'swiper/css'
import 'swiper/css/navigation'
import 'swiper/css/pagination'
import { ref } from 'vue'

const swiper = ref<typeof Swiper | null>(null)

function onSwiper(instance) {
  swiper.value = instance
}

function slideNext() {
  if (swiper.value)
    swiper.value.slideNext()
}

function slidePrev() {
  if (swiper.value)
    swiper.value.slidePrev()
}

function slideToIndex(index) {
  if (swiper.value)
    swiper.value.slideTo(index)
}

const articles = [
  {
    title: 'ELC00696',
    text: 'Код поставщика',
    id: 1,
  },
  {
    title: 'ELC00696',
    text: 'Код РАЭК',
    id: 2,
  },
  {
    title: 'Electric used',
    text: 'Бренд',
    id: 3,
  },
  {
    title: 'ELC0200000696',
    text: 'Код производителя',
    id: 4,
  },
  {
    title: 'ELC0200000696',
    text: 'Артикул',
    id: 5,
  },
  {
    title: 'ELC00696',
    text: 'Код ЕТМ',
    id: 6,
  },
  {
    title: 'ELC00696',
    text: 'Серия',
    id: 7,
  },
]

const slides = [
  {
    img: '/public/slider-1.png',
    id: 1,
  },
  {
    img: '/public/slider-1.png',
    id: 2,
  },
  {
    img: '/public/slider-1.png',
    id: 3,
  },
]
</script>

<template>
  <div class="card-title">
    <Breadcrumbs />
    <h2 class="title">
      Кроссовки мужские Skechers Sunny Dale
    </h2>
  </div>
  <div class="card">
    <div class="card__slider-cont">
      <div class="slider">
        <Swiper
          :slides-per-view="1"
          :navigation="{ nextEl: '.swiper-button-prev', prevEl: '.swiper-button-prev' }"
          :pagination="{ clickable: true }"
          :space-between="50"
          class="js-slider"
          @swiper="onSwiper"
        >
          <SwiperSlide v-for="item in slides" :key="item.id" class="slider__item">
            <img alt="" height="" :src="item.img" width="">
          </SwiperSlide>
        </Swiper>
      </div>
      <div class="slider-navigation">
        <button aria-label="" class="button button--lightblue button--prev" @click="slidePrev()" />
        <div class="slider-navigation__wrapper">
          <button v-for="(item, index) in slides" :key="item.id" aria-label="" class="slider-navigation__item" @click="slideToIndex(index)">
            <img alt="" height="" :src="item.img" width="">
          </button>
        </div>
        <button aria-label="" class="button button--lightblue button--next" @click="slideNext()" />
      </div>
    </div>
    <div class="card__content">
      <div class="card__characteristics">
        <div class="card__settings-cont">
          <div class="card__settings-group">
            <div class="price">
              <span class="price__old">166 534.00 цена без скидки</span>
              <div class="price__current">
                <span class="price__sum">122 566 ₽</span>
                <div class="price__discount">
                  - 15%
                </div>
              </div>
            </div>
            <div class="card__settings">
              <span class="card__amount">12 штук в уп.</span>
              <div class="card__switch">
                <label class="switch">
                  <input type="checkbox" checked>
                  <span class="switch__slider round" />
                </label>
                Заказ упаковкой
              </div>
            </div>
          </div>
          <div class="card__settings-line" />
          <div class="card__info">
            <div class="card__info-item">
              <div class="card__info-item-title">
                Завтра
              </div>
              <div class="card__info-item-text">
                Доставка
              </div>
            </div>
            <div class="card__info-item">
              <div class="card__info-item-title">
                7 шт.
              </div>
              <div class="card__info-item-text">
                Тарасовка
              </div>
            </div>
            <div class="card__info__item">
              <div class="card__info-item-title">
                7 шт.
              </div>
              <div class="card__info-item-text">
                Тарасовка
              </div>
            </div>
          </div>
          <div class="card__buttons">
            <button class="button button--blue button--card-cart">
              В корзину
            </button>
            <button aria-label="" class="button button--lightblue button--card-favorite" />
          </div>
        </div>
        <div class="card__line" />
        <div class="card__values">
          <h4 class="card__values-title">
            Характеристики
          </h4>
          <div class="card__values-list">
            <div v-for="item in articles" :key="item.id" class="card__values-item">
              <div class="card__values-item-title">
                {{ item.title }}
              </div>
              <div lass="card__values-item-text">
                {{ item.text }}
              </div>
            </div>
          </div>
        </div>
      </div>
      <div class="card__description">
        <h3 class="card__title">
          Описание товара
        </h3>
        <p class="card__text">
          Создание приверженного покупателя специфицирует неопровержимый комплексный анализ ситуации. CTR существенно индуцирует из ряда вон выходящий SWOT-анализ. Воздействие на потребителя определяет возрастающий интеграл по поверхности, что известно даже школьникам. Отсюда естественно следует, что коммуникация уравновешивает косвенный фактор коммуникации. Поле направлений естественно допускает экспериментальный скачок функции, таким образом сбылась мечта идиота - утверждение полностью доказано. Арифметическая прогрессия притягивает линейно зависимый пул лояльных изданий.
        </p>
      </div>
    </div>
  </div>
</template>

<style scoped lang="scss">
  .card-title {
    display: flex;
    flex-direction: column;
    gap: 24px;
  }

  .title {
    color: #071435;
    font-size: 32px;
    font-weight: 400;
    line-height: 32px;
    text-transform: uppercase;
  }

  .card {
    display: flex;
    gap: 24px;

    &__slider-cont {
      display: flex;
      flex-direction: column;
      gap: 24px;
      width: 400px;
    }

    &__content {
      display: flex;
      flex-direction: column;
      flex-grow: 1;
      gap: 48px;
    }

    &__sliders {
      display: flex;
      flex-direction: column;
      gap: 24px;
      width: 400px;
    }

    &__characteristics {
        display: flex;
        gap: 48px;
    }

    &__settings-cont {
      display: flex;
      flex-direction: column;
      gap: 32px;
    }

    &__settings-group {
      display: flex;
      flex-direction: column;
      gap: 32px;
    }

    &__settings {
      align-items: center;
      display: flex;
      gap: 16px;
    }

    &__amount {
      background: #F2F5F9;
      color: #828EAD;
      border-radius: 8px;
      font-size: 14px;
      font-weight: 700;
      line-height: 16px;
      padding: 5px 8px;
    }

    &__switch {
      align-items: center;
      color: #071435;
      display: flex;
      font-size: 14px;
      font-weight: 500;
      gap: 12px;
      line-height: 16px;
    }

    &__settings-line {
      background: #E2E4F0;
      height: 1px;
      width: 100%;
    }

    &__info {
      display: flex;
      gap: 16px;
    }

    &__info-item {
      display: flex;
      flex-direction: column;
      gap: 4px;
      width: calc(100% / 3 - 2px);
    }

    &__info-item-title {
      color: #071435;
      font-size: 14px;
      font-weight: 700;
      line-height: 16px;
    }

    &__info-item-text {
        color: #828EAD;
        font-size: 12px;
        font-weight: 400;
        line-height: 16px;
    }

    &__line {
      background: #E2E4F0;
      height: 100%;
      width: 1px;
    }

    &__buttons {
      align-items: center;
      display: flex;
      gap: 16px;
    }

    &__values {
      display: flex;
      flex-direction: column;
      flex-grow: 1;
      gap: 32px;
    }

    &__values-title {
      color: #071435;
      font-size: 20px;
      font-weight: 500;
      line-height: 20px;
    }

    &__values-list {
      column-count: 2;
      column-gap: 32px;
      max-width: 636px;
    }

    &__values-item {
      break-inside: avoid;
      display: flex;
      flex-direction: column;
      gap: 8px;
      margin-bottom: 24px;
      max-width: 302px;
      page-break-inside: avoid;
    }

    &__values-item-title {
      color: #071435;
      font-size: 14px;
      font-weight: 700;
      line-height: 16px;
    }

    &__values-item-text {
      color: #828EAD;
      font-size: 12px;
      font-weight: 400;
      line-height: 16px;
    }

    &__title {
      font-weight: 500;
      font-size: 20px;
      line-height: 20px;
      color: #071435;
    }

    &__description {
      display: flex;
      flex-direction: column;
      gap: 24px;
    }

    &__title {
      color: #071435;
      font-size: 24px;
      line-height: 28px;
      font-weight: 500;
    }

    &__text {
      color: #071435;
      font-size: 18px;
      font-weight: 400;
      line-height: 28px;
    }

  }

  .price {
      display: flex;
      flex-direction: column;
      gap: 24px;

      &__old {
        color: #FF3D71;
        font-size: 14px;
        font-weight: 500;
        line-height: 16px;
      }

      &__current {
        align-items: center;
        display: flex;
        gap: 16px;
      }

        &__sum {
          color: #071435;
          font-size: 32px;
          line-height: 22px;
          letter-spacing: .01em;
          font-weight: 700;
        }

        &__discount {
          background: #FF3D71;
          color: #FFFFFF;
          border-radius: 4px;
          font-size: 16px;
          font-weight: 700;
          line-height: 20px;
          padding: 2px 8px;
        }
  }

  .switch {
      height: 24px;
      position: relative;
      width: 40px;

      input {
          display: none;

          &:checked + .switch__slider {
              background: #1551E5;
          }

          &:focus + .switch__slider {
            box-shadow: 0 0 1px #1551E5;
          }

          &:checked + .switch__slider:before {
              transform: translateX(16px);
          }
      }

      &__slider {
        background: #CCCCCC;
        bottom: 0;
        cursor: pointer;
        left: 0;
        position: absolute;
        right: 0;
        top: 0;
        transition: .3s;

        &:before {
          background: #FFFFFF;
          bottom: 2px;
          content: "";
          height: 20px;
          left: 2px;
          position: absolute;
          transition: .3s;
          width: 20px;
        }
      }

      .round {
        border-radius: 32px;

        &:before {
          border-radius: 50%;
        }
      }
  }

  .slider {
      background: #F2F5F9;
      border-radius: 32px;
      display: flex;
      overflow: hidden;

      &__item {
        height: 400px;
        width: 400px;

        img {
          height: 100%;
          object-fit: contain;
          width: 100%;
        }
      }
  }

  .slider-navigation {
    align-items: center;
    display: flex;
    gap: 16px;

      &__wrapper {
        align-items: center;
        display: flex;
        gap: 12px;
        justify-content: center;
        width: 100%;
      }

      &__item {
        border-radius: 16px;
        height: 64px;
        overflow: hidden;
        width: 64px;
      }

      img {
          height: 100%;
          object-fit: contain;
          width: 100%;
      }
  }
</style>
