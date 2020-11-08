<template>
    <div id="app">
        <div></div>
        <header-colors/>
        <router-view/>
    </div>
</template>

<script>
    import HeaderColors from '../src/components/HeaderColors.vue'

    export default {
        data() {
            return {}
        },
        components: {
            HeaderColors
        }
    }
</script>

<style lang="scss">

    * {
        font-family: Inter, Arial, sans-serif;
        font-size: 16px;
        line-height: 21px;
        -webkit-font-smoothing: antialiased;
        -moz-osx-font-smoothing: grayscale;
        color: #1F2020;
        margin: 0;

    }

    *:link {
        text-decoration: none;
    }

    * button {
        border: none;
        background-color: transparent;
    }

    .blur {
        position: absolute;
        content: '';
        background-color: #000;
        opacity: 0.7;
        width: 100%;
        height: 2000px;
        z-index: 1;
        top: 0;
        left: 0;
    }

    .visually-hidden {
        border: 0;
        clip: rect(0 0 0 0);
        clip-path: inset(100%);
        height: 1px;
        margin: -1px;
        overflow: hidden;
        padding: 0;
        position: absolute;
        white-space: nowrap;
        width: 1px;
    }
</style>
