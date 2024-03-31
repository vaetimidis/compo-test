<script setup lang="ts">
const articles = [
  {
    title: 'ELC00696',
    subtitle: 'Код поставщика',
    id: 1,
  },
  {
    title: 'ELC00696',
    subtitle: 'Код РАЭК',
    id: 2,
  },
  {
    title: 'Electric used',
    subtitle: 'Бренд',
    id: 3,
  },
  {
    title: 'ELC0200000696',
    subtitle: 'Код производителя',
    id: 4,
  },
  {
    title: 'ELC0200000696',
    subtitle: 'Артикул',
    id: 5,
  },
  {
    title: 'ELC00696',
    subtitle: 'Код ЕТМ',
    id: 6,
  },
  {
    title: 'ELC00696',
    subtitle: 'Серия',
    id: 7,
  },
]
</script>

<template>
  <h1 class="title">
    Кроссовки мужские Skechers Sunny Dale
  </h1>
  <div class="card">
    <div class="card__slider">
      asd
    </div>
    <div class="card__content">
      <div class="characteristics">
        <div class="characteristics__settings">
          <div class="characteristics__settings_top">
            <div class="price">
              <span class="price__old">166 534.00 цена без скидки</span>
              <div class="price__current">
                <span class="price__sum">122 566 ₽</span>
                <div class="price__discount">
                  - 15%
                </div>
              </div>
            </div>
            <div class="settings">
              <span class="settings__amount">12 штук в уп.</span>
              <label class="switch">
                <input type="checkbox">
                <span class="switch__slider round" />
              </label>
              <span class="settings__text">Заказ упаковкой</span>
            </div>
          </div>
          <div class="characteristics__settings_bottom">
            <div class="order-info">
              <div class="order-info__item">
                <h6 class="order-info__item_top">
                  Завтра
                </h6>
                <span class="order-info__item_bottom">Доставка</span>
              </div>
              <div class="order-info__item">
                <h6 class="order-info__item_top">
                  7 шт.
                </h6>
                <span class="order-info__item_bottom">Тарасовка</span>
              </div>
              <div class="order-info__item">
                <h6 class="order-info__item_top">
                  7 шт.
                </h6>
                <span class="order-info__item_bottom">Тарасовка</span>
              </div>
            </div>
            <div class="buttons">
              <button class="counter">
                <div class="counter__cart">
                  <img src="/public/cart-white.svg" alt="cart">
                  <span class="couner__text">В корзину</span>
                </div>
              </button>
              <button class="heart">
                <img src="/public/heart.svg" alt="heart">
              </button>
            </div>
          </div>
        </div>
        <div class="characteristics__values">
          <h4 class="characteristics__title">
            Характеристики
          </h4>
          <div class="article">
            <div v-for="item in articles" :key="item.id" class="article__item">
              <h6 class="article__title">
                {{ item.title }}
              </h6>
              <div lass="article__subtitle">
                {{ item.subtitle }}
              </div>
            </div>
          </div>
        </div>
      </div>
      <div class="card__description">
        <h2 class="card__title">
          Описание товара
        </h2>
        <p class="card__text">
          Создание приверженного покупателя специфицирует неопровержимый комплексный анализ ситуации. CTR существенно индуцирует из ряда вон выходящий SWOT-анализ. Воздействие на потребителя определяет возрастающий интеграл по поверхности, что известно даже школьникам. Отсюда естественно следует, что коммуникация уравновешивает косвенный фактор коммуникации. Поле направлений естественно допускает экспериментальный скачок функции, таким образом сбылась мечта идиота - утверждение полностью доказано. Арифметическая прогрессия притягивает линейно зависимый пул лояльных изданий.
        </p>
      </div>
    </div>
  </div>
</template>

<style scoped lang="scss">
    .title {
        font-weight: 400;
        font-size: 32px;
        line-height: 32px;
        margin: 24px 0 32px
    }

    .card {
        display: flex;
        flex-direction: row;

        &__slider {
            display: flex;
            min-width: 400px;
            border: 0.5px solid black;
        }

        &__content {
            display: flex;
            flex-direction: column;
            padding-left: 48px;
            gap: 48px;
        }

        &__description {
          display: flex;
          flex-direction: column;
          gap: 24px;
        }

        &__title {
          font-weight: 500;
          font-size: 24px;
          line-height: 28px;
          color: #071435;
        }

        &__text {
          font-weight: 400;
          font-size: 18px;
          line-height: 28px;
          color: #071435;
        }
    }

    .characteristics {
        display: flex;
        flex-direction: row;
        gap: 48px;

        &__settings {
          display: flex;
          flex-direction: column;
          gap: 32px;

          &_top {
            display: flex;
            flex-direction: column;
            padding-bottom: 32px;
            gap: 32px;
          }

          &_bottom {
            display: flex;
            flex-direction: column;
          }
        }

        &__values {
          display: flex;
          flex-direction: column;
          gap: 32px;
        }

        &__title {
          font-weight: 500;
          font-size: 20px;
          line-height: 20px;
          color: #071435;
        }
    }

    .price {
      display: flex;
      flex-direction: column;
      gap: 24px;

      &__old {
        color: #FF3D71;
        font-weight: 500;
        font-size: 14px;
        line-height: 16px;
      }

      &__current {
        display: flex;
        flex-direction: row;
        align-items: center;
        gap: 16px;
      }

       &__sum {
          font-size: 32px;
          line-height: 48px;
          letter-spacing: 1%;
          font-weight: 700;
        }

        &__discount {
          color: #FFFFFF;
          border-radius: 4px;
          padding: 2px 8px;
          height: 22px;

          font-size: 16px;
          font-weight: 700;
          line-height: 20px;

          background-color: #FF3D71;

          display: flex;
          align-items: center;
          justify-content: center;
        }
    }

    .settings {
      display: flex;
      flex-direction: row;
      align-items: center;
      gap: 16px;

      &__amount {
        padding: 8px;
        border-radius: 8px;
        display: flex;
        gap: 10px;

        background-color: #F2F5F9;
        color: #828EAD;
        line-height: 16px;
        font-size: 14px;
        font-weight: 700;
      }

      &__text {
        font-weight: 500;
        font-size: 14px;
        line-height: 16px;
      }
    }

    .switch {
        position: relative;
        display: inline-block;
        width: 40px;
        height: 24px;

        input {
            display:none;

            &:checked + .switch__slider {
                background-color: #1551E5;
            }

            &:focus + .switch__slider {
                box-shadow: 0 0 1px #1551E5;
            }

            &:checked + .switch__slider:before {
                -webkit-transform: translateX(16px);
                -ms-transform: translateX(16px);
                transform: translateX(16px);
            }
        }

        &__slider {
            position: absolute;
            cursor: pointer;
            top: 0;
            left: 0;
            right: 0;
            bottom: 0;
            background-color: #ccc;
            -webkit-transition: .4s;
            transition: .4s;

            &::before {
                position: absolute;
                content: "";
                height: 16px;
                width: 16px;
                left: 4px;
                bottom: 4px;
                background-color: white;
                -webkit-transition: .4s;
                transition: .4s;
            }
        }

        .round {
        border-radius: 32px;

            &::before {
            border-radius: 50%;
            }
        }
    }

    .order-info {
      display: flex;
      flex-direction: row;
      align-items: center;
      gap: 16px;
      margin-bottom: 32px;

      &__item {
        display: flex;
        flex-direction: column;
        gap: 4px;
        width: 114px;
        height: 40px;

        &_top {
          font-weight: 700;
          font-size: 14px;
          line-height: 16px;
        }

        &_bottom {
          font-weight: 400;
          font-size: 12px;
          line-height: 16px;
          color: #828EAD;
        }
      }
    }

    .buttons {
      display: flex;
      flex-direction: row;
      align-items: center;
      justify-content: flex-start;
      gap: 24px;
    }

    .counter {
      display: flex;
      flex-direction: row;
      align-items: center;
      justify-content: center;
      width: 284px;
      height: 56px;

      background-color: #1551E5;
      color: #fff;
      padding: 16px 24px;
      border-radius: 8px;

      &__cart {
        display: flex;
        flex-direction: row;
        align-items: center;
        justify-content: center;
        gap: 12px;
      }
    }

    .heart {
      display: flex;
      flex-direction: row;
      align-items: center;
      justify-content: center;

      background-color: #F2F6FF;
      padding: 16px 24px;
      border-radius: 8px;
      width: 72px;
      height: 56px;
    }

    .article {
      display: flex;
      flex-direction: column;
      flex-wrap: wrap;
      gap: 24px;
      max-height: 294px;

      &__item {
        display: flex;
        flex-direction: column;
        gap: 8px;
        height: 44px;
      }

      &__title {
        font-weight: 700;
        font-size: 14px;
        line-height: 16px;
        color: #071435;
      }

      &__subtitle {
        font-weight: 400;
        font-size: 12px;
        line-height: 16px;
        color: #828EAD;
      }
    }
</style>
