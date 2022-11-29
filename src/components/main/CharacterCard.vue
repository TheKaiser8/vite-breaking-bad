<script>
export default {
    name: 'CharacterCard',
    props: {
        info: Object,
    }
}
</script>

<template>
   <div class="ms-card text-center p-3 m-3">
        <img class="img-fluid" :src="info.img" :alt="info.name">
        <h5 class="fs-6 fw-bold my-3 ">{{ info.name }}</h5>
        <p class="mb-0 ms-text-grey">{{ info.category }}</p>
        <small class="ms-text-grey">{{ info.status }}</small>
   </div>
</template>

<style lang="scss" scoped>
.ms-card {
    background-color: #2e3a46;
    
    .ms-text-grey {
        color: lightgrey;
    }
}
</style>