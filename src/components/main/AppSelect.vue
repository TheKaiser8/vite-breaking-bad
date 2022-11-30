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
            <option value="" selected>Select category</option>
            <option value="Breaking Bad">Breaking Bad</option>
            <option value="Breaking Bad, Better Call Saul">Breaking Bad, Better Call Saul</option>
        </select>
   </form>
</template>

<style lang="scss" scoped>
</style>