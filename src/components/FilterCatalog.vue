<template>
    <div class="filter">
        <ul class="filter__list">
            <li class="filter__item filter-checkbox">
                <input class="filter-checkbox__input" type="checkbox" name="filter-catalog" id="filter-new" checked>
                <label class="filter-checkbox__label" for="filter-new" >Новинки</label>
            </li>
            <li class="filter__item filter-checkbox">
                <input class="filter-checkbox__input" type="checkbox" name="filter-catalog" id="filter-availability">
                <label class="filter-checkbox__label" for="filter-availability">Есть в наличии</label>
            </li>
            <li class="filter__item filter-checkbox">
                <input class="filter-checkbox__input" type="checkbox" name="filter-catalog" id="filter-contract">
                <label class="filter-checkbox__label" for="filter-contract">Контрактные</label>
            </li>
            <li class="filter__item filter-checkbox">
                <input class="filter-checkbox__input" type="checkbox" name="filter-catalog" id="filter-exclusive">
                <label class="filter-checkbox__label" for="filter-exclusive">Эксклюзивные</label>
            </li>
            <li class="filter__item filter-checkbox">
                <input class="filter-checkbox__input" type="checkbox" name="filter-catalog" id="filter-sale">
                <label class="filter-checkbox__label" for="filter-sale">Распродажа</label>
            </li>
        </ul>
    </div>
</template>

<script>
    export default {
        data() {
            return {
            }
        }
    };
</script>

<style scoped lang="scss">
    .filter {
        flex-grow: 1;
        min-width: 200px;

        &__list {
            padding: 0;
            list-style: none;
        }

        &__item {
            position: relative;
            margin-bottom: 20px;
            height: 25px;
        }
    }

    .filter-checkbox {
        &__input {
            display: none;

            & + label::before {
                position: absolute;
                content: "";
                left: 0px;
                width: 36px;
                height: 23px;
                border-radius: 40px;
                background: #F2F2F2;
            }

            & + label::after {
                position: absolute;
                content: "";
                left: 7px;
                width: 8px;
                height: 8px;
                top: 7px;
                background: #1F2020;
                border-radius: 50%;
            }

            &:checked + label::before {
                background:  #7BB899;
            }

            &:checked + label::after {
                left: 21px;
            }

        }

        &__label {
            font-style: normal;
            font-weight: normal;
            font-size: 12px;
            line-height: 100%;
            letter-spacing: 0.06em;
            text-transform: uppercase;
            color: #1F2020;
            padding-left: 60px;
        }
    }


</style>