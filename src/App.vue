<script>
import AppHeader from './components/header/AppHeader.vue';
import AppMain from './components/main/AppMain.vue';

export default {
    components: {
    AppHeader,
    AppMain,
    } 
}
</script>

<template>
    <body>
        <AppHeader/>
        
        <AppMain/>        
    </body>
</template>

<style lang="scss">
@import './style/global.scss';
body {
    background-color: #2e3a46;
}
</style>
