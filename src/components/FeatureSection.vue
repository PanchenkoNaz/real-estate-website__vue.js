<template>
  <section class="section feature" aria-labelledby="feature-label">
    <div class="container">
      <figure class="feature-banner">
        <img src="@/assets/images/feature-banner-1.jpg" width="1020" height="690" loading="lazy" alt="feature banner" class="img-cover" />
      </figure>

      <div class="feature-content">
        <h2 class="headline-medium" id="feature-label">
          We Specialize In Quality Home Renovations
        </h2>
        <p class="body-large feature-text">
          Looking to renovate your home to reflect your style and personality? Look no further than our team of experts who specialize in quality home renovations to transform your space into a dream home you’ll love. From design to execution.
        </p>
        <ul class="feature-list">
          <li class="feature-item" v-for="(feature, index) in features" :key="index">
            <span class="material-symbols-rounded feature-icon" aria-hidden="true">check_circle</span>
            <span class="body-medium">{{ feature }}</span>
          </li>
        </ul>
      </div>
    </div>
  </section>

  <section class="section feature feature-2" aria-labelledby="feature-label-2">
    <div class="container">
      <figure class="feature-banner">
        <img src="@/assets/images/feature-banner-2.jpg" width="1020" height="690" loading="lazy" alt="feature banner" class="img-cover" />
      </figure>

      <div class="feature-content">
        <h2 class="headline-medium" id="feature-label-2">
          We Are Experts In Historic Home Renovations
        </h2>
        <p class="body-large feature-text">
          Looking to renovate your home to reflect your style and personality? Look no further than our team of experts who specialize in quality home renovations to transform your space into a dream home you’ll love. From design to execution.
        </p>
        <ul class="feature-list">
          <li class="feature-item" v-for="(feature, index) in features" :key="index">
            <span class="material-symbols-rounded feature-icon" aria-hidden="true">check_circle</span>
            <span class="body-medium">{{ feature }}</span>
          </li>
        </ul>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: 'FeatureSection',
  data() {
    return {
      features: [
        "Smart Home",
        "Beautiful Scene Around",
        "Exceptional lifestyle",
        "Complete 24/7 Security"
      ]
    };
  }
};
</script>

<style scoped>
/* Додайте стилі, специфічні для FeatureSection, або залиште стилі в style.css */
</style>
