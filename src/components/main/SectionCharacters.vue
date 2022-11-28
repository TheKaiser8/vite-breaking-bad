<script>
import CharacterCard from './CharacterCard.vue';

export default {
    name: 'SectionCharacters',
    components: {
        CharacterCard,
    }
}
</script>

<template>
    <section id="characters" class="p-5">
        <div class="found-characters ps-3 py-4">
            <span class="fw-bold">Found 62 characters</span>
        </div>
        <div class="d-flex">
            <CharacterCard/>
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

}
</style>