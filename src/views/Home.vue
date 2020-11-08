<template>
    <div class="home">
        <banner/>
        <div class="main">
            <filter-catalog/>
            <main-content/>
        </div>
        <shop/>
    </div>
</template>

<script>
    import Banner from '../components/Banner.vue'
    import FilterCatalog from '../components/FilterCatalog.vue'
    import MainContent from '../components/MainContent.vue'
    import Shop from '../components/Shop.vue'

    export default {
        data() {
            return {}
        },
        components: {
            Banner,
            FilterCatalog,
            MainContent,
            Shop
        }
    }
</script>

<style lang="scss">
    .main {
        padding: 72px 64px;
        display: flex;
        align-items: flex-start;
        justify-content: space-between;
        flex: 3 1 100px;
    }

    @media screen and (max-width: 1250px) {
        .main {
            padding: 30px;
        }
    }

</style>