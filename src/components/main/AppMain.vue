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
    methods: {
        getCharacter() {
            axios.get('https://www.breakingbadapi.com/api/characters', {
                params: {
                    category: this.store.categoryValue,
                }
            })
            .then((response) => {
            this.store.characters = response.data;
            });
        },
    },
    created() {
        this.getCharacter();
    }
}
</script>

<template>
    <main class="container">
        <AppSelect @search="getCharacter" />

        <SectionCharacters/>
    </main>
</template>

<style lang="scss" scoped>
</style>