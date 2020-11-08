<template>
    <div class="product">
        <div class="product__image-container">
            <img class="product__image" src="../assets/img/products/Photo-1.png" alt="#">
        </div>
        <h3 class="product__title">Краска Wallquest, Brownsone MS90102</h3>
        <div class="product__functional">
            <span class="product__functional--price">6000Р</span>
            <button class="product__functional--add">
                <svg class="product__functional--image">
                    <use xlink:href="../assets/img/icons/sprite.svg#icon-plus"></use>
                </svg>
            </button>
        </div>
    </div>
</template>

<script>
    export default {
        data() {
            return {}
        }
    }
</script>

<style scoped lang="scss">
    .product {
        width: 284px;
        height: 378px;
        margin: 16px 24px 14px 0;
        border-bottom: 1px solid #0000001a;

        &__image-container {
            width: 278px;
            height: 278px;
            display: flex;
            align-items: center;
            justify-content: center;
        }

        &__title {
            font-weight: 300;
            font-size: 16px;
            line-height: 18px;
            letter-spacing: 0.02em;
        }

        &__functional {
            display: flex;
            justify-content: space-between;
            align-items: center;

            &--price {
                font-weight: 600;
                font-size: 16px;
                line-height: 100%;
            }

            &--add {
                padding: 6px 30px;
                /*border: none;*/
                width: 80px;
                height: 32px;
                background: #7BB899;
                border-radius: 8px;
            }

            &--image {
                width: 20px;
                height: 20px;
            }
        }
    }
</style>