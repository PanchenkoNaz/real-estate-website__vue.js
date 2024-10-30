<template>
    <header>
        <nav>
            <a href="#">Home</a>
            <a href="#">Rent</a>
            <a href="#">Sell</a>
            <a href="#">Buy</a>
            <a href="#">About</a>
        </nav>
        <button @click="toggleMenu">Menu</button>
    </header>
</template>

<script>
export default {
    methods: {
        toggleMenu() {
            // Логіка для відкриття/закриття меню
        },
    },
};
</script>

<style scoped>
/* Стилі для HeaderComponent */
</style>
