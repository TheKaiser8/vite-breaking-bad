<script>
import axios from 'axios';
import CharacterCard from './CharacterCard.vue';

export default {
    name: 'SectionCharacters',
    components: {
        CharacterCard,
    },
    data() {
        return {
            characters: [],
        }
    },
    created() {
        axios.get('https://www.breakingbadapi.com/api/characters')
        .then((response) => {
            this.characters = response.data;
        })
    }
}
</script>

<template>
    <section id="characters" class="p-5">
        <div class="found-characters ps-3 py-4">
            <span class="fw-bold">Found 62 characters</span>
        </div>
        <div class="d-flex flex-wrap">
            <CharacterCard
            v-for="character in characters"
            :info="character"
            class="character-card"
            />
        </div>
    </section>
</template>

<style lang="scss" scoped>
#characters {
    background-color: #ffffff;
    color: #fff;
    
    .found-characters {
        background-color: #212529;
    }

    .character-card {
        width: calc((100% / 5) - 2rem);
    }
}
</style>