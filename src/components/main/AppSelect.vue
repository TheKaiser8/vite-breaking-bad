<script>
import { store } from '../../store.js';

export default {
    name: 'AppSelect',
    data() {
        return {
            store
        }
    }
}
</script>

<template>
   <form action="" class="ps-3 py-4">
        <select class="form-select w-auto" name="category" v-model="store.categoryValue" @change="$emit('search')">
            <option selected>Select category</option>
            <option value="Breaking Bad">Breaking Bad</option>
            <option value="Breaking Bad, Better Call Saul">Breaking Bad, Better Call Saul</option>
        </select>

        <!-- Prova con select per lo status: -->
        <!-- <select class="form-select w-auto" name="status" v-model="store.statusValue" @change="$emit('search')">
            <option selected>Select status</option>
            <option value="Alive">Alive</option>
            <option value="Deceased">Deceased</option>
            <option value="Presumed dead">Presumed dead</option>
            <option value="Unknown">Unknown</option>
        </select> -->
   </form>
</template>

<style lang="scss" scoped>
</style>