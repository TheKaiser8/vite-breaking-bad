<script>
import AppSelect from './AppSelect.vue';
import SectionCharacters from './SectionCharacters.vue';

export default {
    name: 'AppMain',
    components: {
        AppSelect,
        SectionCharacters,
    }
}
</script>

<template>
    <main class="container">
        <AppSelect/>

        <SectionCharacters/>
    </main>
</template>

<style lang="scss" scoped>
</style>