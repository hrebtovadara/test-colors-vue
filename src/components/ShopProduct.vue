<template>
    <div class="shop-product">
        <img class="shop-product__image" src="../assets/img/products/Photo-1.png" alt="изображение товара">
        <div class="shop-product__info">
            <h3 class="shop-product__title">Краска Wallquest, Brownsone MS90102</h3>
            <span class="shop-product__price">9600 ₽</span>
        </div>
        <div class="shop-product__counter product-counter">
            <button class="product-counter__button product-counter__button--remove"></button>
            <span class="product-counter__counter">2</span>
            <button class="product-counter__button product-counter__button--add"></button>
        </div>
        <button class="shop-product__close visually-hidden">
            <svg class="shop-product__close--image-close">
                <use xlink:href="../assets/img/icons/sprite.svg#icon-close"></use>
            </svg>
        </button>
        <button class="shop-product__close ">
            <svg class="shop-product__close--image-repeat">
                <use xlink:href="../assets/img/icons/sprite.svg#icon-repeat"></use>
            </svg>
        </button>
    </div>
</template>

<script>
    export default {
        name: "ShopProduct.vue"
    }
</script>

<style scoped lang="scss">
    .shop-product {
        padding: 12px 0;
        display: flex;
        align-items: center;
        justify-content: space-between;
        border-bottom: 1px solid #e6e6e6;

        &__image {
            width: 96px;
            height: 96px;
        }

        &__title {
            font-weight: 300;
            font-size: 16px;
            line-height: 18px;
            letter-spacing: 0.02em;
            max-width: 165px;
        }

        &__price {
            font-weight: 600;
            font-size: 16px;
            line-height: 100%;
        }

        &__close {
            width: 24px;
            height: 24px;
            padding: 0;

            &--image-close {
                opacity: .4;
            }

        }

        &:last-child {
            border-bottom: none;
        }

    }

    .product-counter {

        display: flex;
        align-items: center;
        justify-content: center;

        &__button {
            width: 40px;
            height: 24px;
            background: #F2F2F2;
            border-radius: 4px;
            position: relative;
            margin: 0 20px;

            &:before {
                content: '';
                width: 9px;
                height: 1px;
                border-top: 2px solid #000000;
                position: absolute;
                top: 11px;
                left: 15px;
                border-radius: 1px;
            }

            &--add:after {
                content: '';
                width: 9px;
                height: 1px;
                border-top: 2px solid #000000;
                position: absolute;
                top: 11px;
                left: 15px;
                transform: rotate(90deg);
                border-radius: 1px;
            }
        }
    }
</style>