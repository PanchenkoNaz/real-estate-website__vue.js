<template>
    <section class="property-search">
        <h2>Search for Properties</h2>
        <form @submit.prevent="onSearch">
            <input type="text" placeholder="Street, City, Zip..." v-model="location">
            <select v-model="propertyType">
                <option>Any</option>
                <option>Houses</option>
                <option>Apartments</option>
                <option>Villa</option>
                <option>Townhome</option>
            </select>
            <button type="submit">Search</button>
        </form>
    </section>
</template>

<script>
export default {
    data() {
        return {
            location: '',
            propertyType: 'Any'
        };
    },
    methods: {
        onSearch() {
            // Логіка для обробки пошуку
            console.log('Searching for', this.propertyType, 'in', this.location);
        },
    },
};
</script>

<style scoped>
/* Стилі для PropertySearch */
</style>
