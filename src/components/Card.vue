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
            <span class="old-price">166 534.00 цена без скидки</span>
            <span class="price">122 566 ₽</span>
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
                <span class="order-info__item_top">Завтра</span>
                <span class="order-info__item_bottom">Доставка</span>
              </div>
              <div class="order-info__item">
                <span class="order-info__item_top">7 шт.</span>
                <span class="order-info__item_bottom">Тарасовка</span>
              </div>
              <div class="order-info__item">
                <span class="order-info__item_top">7 шт.</span>
                <span class="order-info__item_bottom">Тарасовка</span>
              </div>
            </div>
            <div class="buttons">
              <button class="counter" />
              <button class="heart">
                <img src="/public/heart.svg" alt="heart">
              </button>
            </div>
          </div>
        </div>
        <div class="characteristics__values" />
      </div>
      <div class="card__description">
        <h2>Описание товара</h2>
        <p>Создание приверженного покупателя специфицирует неопровержимый комплексный анализ ситуации. CTR существенно индуцирует из ряда вон выходящий SWOT-анализ. Воздействие на потребителя определяет возрастающий интеграл по поверхности, что известно даже школьникам. Отсюда естественно следует, что коммуникация уравновешивает косвенный фактор коммуникации. Поле направлений естественно допускает экспериментальный скачок функции, таким образом сбылась мечта идиота - утверждение полностью доказано. Арифметическая прогрессия притягивает линейно зависимый пул лояльных изданий.</p>
      </div>
    </div>
  </div>
</template>

<style scoped lang="scss">
    .title {
        font-weight: 400;
        font-size: 32px;
        line-height: 32px;
        margin: 24px 0 32Px
    }

    .card {
        display: flex;
        flex-direction: row;

        &__slider {
            display: flex;
            min-width: 400px
        }

        &__content {
            display: flex;
            flex-direction: column;
        }
    }

    .characteristics {
        display: flex;
        flex-direction: row;

    }

    .switch {
        position: relative;
        display: inline-block;
        width: 60px;
        height: 34px;

        input {
            display:none;

            &:checked + .switch__slider {
                background-color: #1551E5;
            }

            &:focus + .switch__slider {
                box-shadow: 0 0 1px #1551E5;
            }

            &:checked + .switch__slider:before {
                -webkit-transform: translateX(26px);
                -ms-transform: translateX(26px);
                transform: translateX(26px);
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
                height: 26px;
                width: 26px;
                left: 4px;
                bottom: 4px;
                background-color: white;
                -webkit-transition: .4s;
                transition: .4s;
            }
        }

        .round {
        border-radius: 34px;

            &::before {
            border-radius: 50%;
            }
        }
    }
</style>
