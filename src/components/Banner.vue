<template>
    <div class="banner">
        <img class="banner__fon" src="../assets/img/banners/banner-one.jpg" alt="Баннер">
        <ul class="banner__nav nav-banner">
            <li class="nav-banner__item"><a href="#">Главная</a></li>
            <li class="nav-banner__item"><a href="#">Продукты</a></li>
            <li class="nav-banner__item"><a href="#">Краски</a></li>
        </ul>
        <div class="banner__text">
            <p class="banner__text--title">Краски</p>
            <p class="banner__text--description">Идеально подходят для стен и других поверхностей. Найди свой идеальный
                цвет!</p>
        </div>
        <ul class="banner__slider slider">
            <li class="slider__item">
                <input class="slider__input" type="radio" name="slider-banner" id="1" checked>
                <label class="slider__label" for="1"></label>
            </li>
            <li class="slider__item">
                <input class="slider__input" type="radio" name="slider-banner" id="2">
                <label class="slider__label" for="2"></label>
            </li>
            <li class="slider__item">
                <input class="slider__input" type="radio" name="slider-banner" id="3">
                <label class="slider__label" for="3"></label>
            </li>
            <li class="slider__item">
                <input class="slider__input" type="radio" name="slider-banner" id="4">
                <label class="slider__label" for="4"></label>
            </li>
            <li class="slider__item">
                <input class="slider__input" type="radio" name="slider-banner" id="5">
                <label class="slider__label" for="5"></label>
            </li>
            <li class="slider__item">
                <input class="slider__input" type="radio" name="slider-banner" id="6">
                <label class="slider__label" for="6"></label>
            </li>
        </ul>

        <div class="banner__arrow--left">
            <svg>
                <use xlink:href="../assets/img/icons/sprite.svg#icon-arrow"></use>
            </svg>
        </div>
        <div class="banner__arrow--right">
            <svg>
                <use xlink:href="../assets/img/icons/sprite.svg#icon-arrow"></use>
            </svg>
        </div>
    </div>

</template>

<script>
    export default {
        data() {
            return {}
        }
    };
</script>

<style scoped lang="scss">
    .banner {
        width: 100%;
        height: 560px;
        position: relative;
        display: flex;
        flex-direction: column;
        justify-content: center;

        &__fon {
            width: 1920px;
            height: 560px;
            z-index: -1;
            position: absolute;
        }

        &__text {
            width: 472px;
            height: 129px;
            margin: 217px auto 0;
            text-align: center;

            &--title {
                font-size: 72px;
                line-height: 63px;
                letter-spacing: -0.02em;
                color: #FFFFFF;
                margin-bottom: 24px;
            }

            &--description {
                font-weight: 500;
                font-size: 16px;
                line-height: 21px;
                letter-spacing: 0.02em;
                color: #FFFFFF;
            }
        }

        &__arrow--left {
            width: 22px;
            height: 40px;
            position: absolute;
            top: 354px;
            left: 25%;
            transform: scale(-1, 1);
        }

        &__arrow--right {
            width: 22px;
            height: 40px;
            position: absolute;
            top: 354px;
            right: 25%;
        }
    }

    .nav-banner {
        padding: 0;
        display: flex;
        list-style: none;
        position: absolute;
        top: 32px;
        left: 64px;

        &__item {
            position: relative;

            &::before {
                position: absolute;
                content: '';
                width: 3px;
                height: 3px;
                background-color: #FFFFFF;
                opacity: 0.3;
                border-radius: 50%;
                right: 8px;
                top: 50%;
            }

            &:last-child {
                &::before {
                    display: none;
                }
            }

            & a {
                font-size: 10px;
                line-height: 100%;
                letter-spacing: 0.06em;
                text-transform: uppercase;
                color: #FFFFFF;
                opacity: 0.3;
                margin-right: 19px;
            }
        }
    }

    .slider {
        padding: 13px 20px;
        list-style: none;
        display: flex;
        align-items: center;
        justify-content: center;
        min-width: 124px;
        height: 32px;
        background: rgba(0, 0, 0, 0.4);
        border-radius: 16px;
        margin: 143px auto 0;

        &__item {
            margin: 0 4px;
            position: relative;
            width: 6px;
            height: 6px;
        }

        &__input {
            display: none;

            + label::before {
                position: absolute;
                content: " ";
                width: 6px;
                height: 6px;
                background-color: #FFFFFF;
                opacity: 0.2;
                border-radius: 50%;
                top: 0;
                left: 0;
            }

            &:checked,
            &:hover {
                + label::before {
                    opacity: 1;
                }
            }
        }
    }

    @media screen and (max-width: 1250px) {
        .banner {

            &__arrow--left {
                width: 22px;
                height: 40px;
                position: absolute;
                top: 354px;
                left: 5%;
                transform: scale(-1, 1);
            }

            &__arrow--right {
                width: 22px;
                height: 40px;
                position: absolute;
                top: 354px;
                right: 5%;
            }
        }
    }

    @media screen and (max-width: 655px) {
        .nav-banner {
            padding: 0;
            display: flex;
            list-style: none;
            position: absolute;
            top: 32px;
            margin: 0 auto;
        }

        .banner__text {
                width: 300px;
                height: 129px;
                margin: 120px auto 0;
        }
    }
</style>