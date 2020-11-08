<template>
    <div class="header">
        <img class="header__logo" src="../assets/img/logo/colors-logo.png" atl="Логотип colors">
        <nav class="header__nav nav-header">
            <ul class="nav-header__list">
                <li class="nav-header__item">
                    <router-link to="/">Продукты</router-link>
                </li>
                <li class="nav-header__item">
                    <router-link to="/">Цвета</router-link>
                </li>
                <li class="nav-header__item">
                    <router-link to="/">Вдохновение</router-link>
                </li>
                <li class="nav-header__item">
                    <router-link to="/">Советы</router-link>
                </li>
                <li class="nav-header__item">
                    <router-link to="/">Найти магазин</router-link>
                </li>
            </ul>
        </nav>
        <div class="header__feedback">
            <span class="header__feedback--num">+7 (495) 221-77-69</span>
            <button class="header__feedback--button-num">Заказать звонок</button>
        </div>
        <div class="header__menu">
            <button class="header__button">
                <svg class="header__menu--search">
                    <use xlink:href="../assets/img/icons/sprite.svg#icon-search"></use>
                </svg>
            </button>
            <button class="header__button ">
                <svg class="header__menu--profile">
                    <use xlink:href="../assets/img/icons/sprite.svg#icon-profile"></use>
                </svg>
            </button>
            <button class="header__button ">
                <svg class="header__menu--like">
                    <use xlink:href="../assets/img/icons/sprite.svg#icon-like"></use>
                </svg>
            </button>
            <button class="header__button header__menu--shop">4</button>
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
    .header {
        min-height: 104px;
        width: 100%;
        display: flex;
        align-items: center;
        justify-content: space-between;
        padding: 38px 72px 40px 64px;

        &__button {
            /*border: none;*/
            /*background-color: transparent;*/
            display: flex;
            align-items: center;
            justify-content: center;
            margin-left: 20px;
        }

        &__menu {
            display: flex;

            &--shop {
                border-radius: 50%;
                background-color: #7BB899;
                width: 24px;
                height: 24px;
                font-size: 12px;
                font-style: normal;
                font-weight: 500;
                line-height: 15px;
            }

            &--search {
                width: 20px;
                height: 20px;
            }

            &--like,
            &--profile {
                width: 22px;
                height: 22px;
            }
        }

        &__feedback {
            display: flex;
            flex-direction: column;

            &--num {
                font-size: 16px;
                font-weight: 500;
                line-height: 16px;
            }

            &--button-num {
                /*border: none;*/
                /*background-color: transparent;*/
                font-size: 14px;
                font-weight: 400;
                line-height: 14px;
                text-align: left;
                opacity: 0.3;
            }
        }
    }

    .nav-header {
        &__list {
            padding: 0;
            list-style: none;
            display: flex;
            text-transform: uppercase;
        }

        &__item {
            margin-right: 24px;
        }
    }

    @media screen and (max-width: 1250px) {
        .header {
            height: 300px;
            width: 100%;
            flex-direction: column;
            padding: 38px 30px 40px;
        }

        .nav-header {
            &__list {
                display: flex;
            }
        }
    }

    @media screen and (max-width: 655px) {
        .header {
            height: 400px;
            width: 100%;
            min-width: 320px;
            flex-direction: column;
            align-items: center;

            &__button {
                display: flex;
                align-items: center;
                justify-content: center;
                margin: 0 10px;
            }
        }

        .nav-header {
            &__list {
                flex-direction: column;
                align-items: center;
            }

            &__item {
                margin-top: 15px;
            }
        }
    }
</style>
