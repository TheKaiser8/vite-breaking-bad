<script>
import axios from 'axios';
import { store } from '../../store.js';
import AppSelect from './AppSelect.vue';
import SectionCharacters from './SectionCharacters.vue';

export default {
    name: 'AppMain',
    components: {
        AppSelect,
        SectionCharacters,
    },
    data() {
        return {
            store
        }
    },
    created() {
        axios.get('https://www.breakingbadapi.com/api/characters')
        .then((response) => {
            this.store.characters = response.data;
        })
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