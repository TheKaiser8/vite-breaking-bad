<script>
import AppHeader from './components/AppHeader.vue';

export default {
    components: {
    AppHeader,
    } 
}
</script>

<template>
    <body>
        <AppHeader/>
    </body>
</template>

<style lang="scss">
@import './style/global.scss';
body {
    background-color: #2e3a46;
}
</style>
