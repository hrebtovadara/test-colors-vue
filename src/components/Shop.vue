<template>
    <div class="shop visually-hidden">
        <div class="shop__container">
            <div class="shop__header">
                <h2 class="shop__title">Корзина</h2>
                <button class="shop__close">
                    <svg class="shop__close--image">
                        <use xlink:href="../assets/img/icons/sprite.svg#icon-close"></use>
                    </svg>
                </button>
            </div>
            <div class="shop__catalog shop-catalog">
                <div class="shop-catalog__header">
                    <span class="shop-catalog__quantity">4 товара</span>
                    <button class="shop-catalog__clear">очистить список</button>
                </div>
            </div>
            <ul class="shop__list">
                <shop-product></shop-product>
                <shop-product></shop-product>
                <shop-product></shop-product>
            </ul>
        </div>
        <div class="shop__footer">
            <p class="shop__footer-container">
                <span class="shop__footer--end">Итого</span>
                <span class="shop__footer--price">14 400₽</span>
            </p>
            <button class="shop__footer-button">Оформить заказ</button>
        </div>
    </div>
</template>

<script>
    import ShopProduct from "../components/ShopProduct.vue"

    export default {
        data() {
            return {}
        },
        components: {
            ShopProduct
        }
    }
</script>

<style scoped lang="scss">
    .shop {
        position: absolute;
        right: 0;
        top: 0;
        width: 600px;
        height: 100%;
        padding: 32px 40px;
        background-color: #FFFFFF;
        z-index: 2;
        display: flex;
        justify-content: space-between;
        flex-direction: column;

        &__header {
            display: flex;
            align-items: center;
            justify-content: space-between;
        }

        &__title {
            font-weight: 500;
            font-size: 30px;
            line-height: 26px;
            letter-spacing: -0.04em;
        }

        &__close {
            border: 1px solid #e6e6e6;
            border-radius: 50%;
            box-sizing: border-box;
            padding: 13px;
            width: 48px;
            height: 48px;
            background-color: transparent;

            &--image {
                width: 20px;
                height: 20px;
            }
        }

        &__list {
            padding: 0;
            list-style: none;
        }

        &__footer {
            display: flex;
            align-items: center;
            justify-content: space-between;

            &-container {
                display: flex;
                flex-direction: column;
            }

            &--price {
                font-weight: 500;
                font-size: 30px;
                line-height: 30px;
                letter-spacing: -0.02em;
            }

            &-button {
                width: 240px;
                height: 56px;
                background: #7BB899;
                border-radius: 4px;
                font-weight: 500;
                font-size: 12px;
                line-height: 15px;
                letter-spacing: 0.06em;
                text-transform: uppercase;
            }
        }
    }

    .shop-catalog {

        border-bottom: 1px solid #e6e6e6;

        &__header {
            display: flex;
            align-items: center;
            justify-content: space-between;
        }

        &__clear {
            /*border: none;*/
            /*background-color: transparent;*/
            color: #1F2020;
            opacity: 0.4;
            font-weight: 300;
        }
    }
</style>