<template>
    <div>
        <HeaderComponent />
        <HeroSection />
        <PropertySearch />
        <FooterComponent />
    </div>
</template>

<script>
import HeaderComponent from './components/HeaderComponent.vue';
import HeroSection from './components/HeroSection.vue';
import PropertySearch from './components/PropertySearch.vue';
import FooterComponent from './components/FooterComponent.vue';

export default {
    components: {
        HeaderComponent,
        HeroSection,
        PropertySearch,
        FooterComponent,
    },
};
</script>

<style>
/* Додаткові глобальні стилі, якщо потрібно */
</style>
