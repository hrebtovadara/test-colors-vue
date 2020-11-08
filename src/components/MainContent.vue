<template>
    <div class="catalog">
        <div class="catalog-header">
            <span class="catalog-header__quantity">412 товаров</span>
            <div class="catalog-header__sort catalog-sort">
                <button class="catalog-sort__button">Сначала дорогие</button>
                <ul class="catalog-sort__list visually-hidden">
                    <li class="catalog-sort__item">
                        <button class="catalog-sort__item--button">Сначала дорогие</button>
                    </li>
                    <li class="catalog-sort__item">
                        <button class="catalog-sort__item--button">Сначала недорогие</button>
                    </li>
                    <li class="catalog-sort__item">
                        <button class="catalog-sort__item--button">Сначала популярные</button>
                    </li>
                    <li class="catalog-sort__item">
                        <button class="catalog-sort__item--button">Сначала новые</button>
                    </li>
                </ul>
            </div>
        </div>
        <div class="catalog-container">
            <ul class="catalog-container__list">
                <product/>
                <product/>
                <product/>
                <product/>
                <product/>
                <product/>
            </ul>
        </div>
    </div>
</template>

<script>
    import Product from "../components/Product.vue"

    export default {
        data() {
            return {}
        },
        components: {
            Product
        }
    }
</script>

<style scoped lang="scss">
    .catalog {
        flex-grow: 9;
        position: relative;
    }

    .catalog-header {
        display: flex;
        align-items: center;
        justify-content: space-between;
        text-transform: uppercase;
        color: #1F2020;

        &__quantity {
            font-weight: 500;
            font-size: 12px;
            line-height: 15px;
            letter-spacing: 0.06em;
        }
    }

    .catalog-sort {

        &__button {
            /*border: none;*/
            /*background-color: transparent;*/
            text-transform: uppercase;
            position: relative;
            font-weight: 500;
            font-size: 12px;
            line-height: 15px;
            letter-spacing: 0.06em;

            &:after {
                position: absolute;
                content: "";
                top: 6px;
                right: -4px;
                width: 0;
                height: 0;
                border-left: 4px solid transparent;
                border-right: 4px solid transparent;
                border-top: 5px solid black;
            }

        }

        &__list {
            width: 280px;
            height: 198px;
            padding: 0;
            list-style: none;
            position: absolute;
            top: 0px;
            right: 0;
        }

        &__item {
            &--button {
                /*border: none;*/
                background-color: #FFFFFF;
                width: 280px;
                height: 48px;
                font-weight: 500;
                font-size: 12px;
                line-height: 15px;
                letter-spacing: 0.06em;
                text-transform: uppercase;

                &:hover {
                    background-color:#7BB899;
                }
            }
        }
    }

    .catalog-container {
        padding-top: 40px;

        &__list {
            display: flex;
            flex-wrap: wrap;
            align-items: flex-start;
            justify-content: space-between;
        }
    }

    @media screen and (max-width: 1250px) {

        .catalog-header {
            align-items: center;
        }

        .catalog-container {
            padding-top: 20px;
        }
    }

</style>