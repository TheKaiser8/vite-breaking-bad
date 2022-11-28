<script>
export default {
    name: 'AppHeader',
}
</script>

<template>
    <header class="d-flex align-items-center p-3">
        <img src="../assets/img/logo.png" alt="Logo Breaking Bad">
        <h1>Breaking Bad Api</h1>
    </header>
</template>

<style lang="scss" scoped>
header {
    color: #fff;
    img {
        max-height: 2rem;
    }
    h1 {
        line-height: 2rem;
    }
}
</style>
