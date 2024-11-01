<template>
  <section class="hero">
    <div class="container">
      <div class="hero-content">
        <h1 class="headline-large hero-title">Find a place where you can be yourself.</h1>
        <p class="body-large hero-text">
          If you're looking for a place where you can be yourself, don't give up. Keep searching until you find a place that feels like home.
        </p>
        <form action="./" method="get" class="search-bar">
          <label class="search-item">
            <span class="label-medium label">Want to</span>
            <select name="want-to" class="search-item-field body-medium">
              <option value="buy" selected>Buy</option>
              <option value="sell">Sell</option>
              <option value="rent">Rent</option>
            </select>
            <span class="material-symbols-rounded" aria-hidden="true">real_estate_agent</span>
          </label>
          <label class="search-item">
            <span class="label-medium label">Property type</span>
            <select name="property-type" class="search-item-field body-medium">
              <option value="any" selected>Any</option>
              <option value="houses">Houses</option>
              <option value="apartments">Apartments</option>
              <option value="villa">Villa</option>
              <option value="townhome">Townhome</option>
              <option value="bungalow">Bungalow</option>
              <option value="loft">Loft</option>
            </select>
            <span class="material-symbols-rounded" aria-hidden="true">gite</span>
          </label>
          <label class="search-item">
            <span class="label-medium label">Location</span>
            <input type="text" name="location" placeholder="Street, City, Zip..." class="search-item-field body-medium" />
            <span class="material-symbols-rounded" aria-hidden="true">location_on</span>
          </label>
          <button type="submit" class="search-btn">
            <span class="material-symbols-rounded" aria-hidden="true">search</span>
            <span class="label-medium">Search</span>
          </button>
        </form>
      </div>
      <img src="@/assets/images/hero.png" width="816" height="659" role="presentation" class="hero-banner" />
      <img src="@/assets/images/bg-pattern.png" width="1240" height="840" role="presentation" class="bg-pattern" />
    </div>
  </section>
</template>

<script>
export default {
  name: 'HeroSection'
};
</script>

<style scoped>
/* Додайте стилі, специфічні для HeroSection, або залиште стилі в style.css */
</style>
