<template>
  <div id="app">
    <HeaderComponent />
    <HeroSection />
    <PropertySection />
    <FeatureSection />
    <VideoSection />
    <StorySection />
    <FooterComponent />
  </div>
</template>

<script>
import HeaderComponent from './components/HeaderComponent.vue';
import HeroSection from './components/HeroSection.vue';
import PropertySection from './components/PropertySection.vue';
import FeatureSection from './components/FeatureSection.vue';
import VideoSection from './components/VideoSection.vue';
import StorySection from './components/StorySection.vue';
import FooterComponent from './components/FooterComponent.vue';

export default {
  components: {
    HeaderComponent,
    HeroSection,
    PropertySection,
    FeatureSection,
    VideoSection,
    StorySection,
    FooterComponent
  }
};
</script>

<style>
/* Глобальні стилі, якщо необхідно */
</style>
