<template>
  <header class="header" data-header>
    <div class="container">
      <a href="#" class="logo">
        <img src="/src/assets/images/logo.png" width="190" height="28" alt="wealthome" />
      </a>

      <nav class="navbar" data-navbar>
        <ul class="navbar-list">
          <li><a href="#" class="navbar-link label-medium active">Home</a></li>
          <li><a href="#" class="navbar-link label-medium">Rent</a></li>
          <li><a href="#" class="navbar-link label-medium">Sell</a></li>
          <li><a href="#" class="navbar-link label-medium">Buy</a></li>
          <li><a href="#" class="navbar-link label-medium">About</a></li>
        </ul>

        <div class="navbar-wrapper">
          <a href="#" class="btn-link label-medium">Login</a>
          <a href="#" class="btn btn-fill label-medium">Get Started</a>
        </div>
      </nav>

      <button class="nav-toggle-btn icon-btn" aria-label="toggle navbar" data-nav-toggler>
        <span class="material-symbols-rounded open" aria-hidden="true">menu</span>
        <span class="material-symbols-rounded close" aria-hidden="true">close</span>
      </button>
    </div>
  </header>
</template>

<script>
export default {
  name: 'HeaderComponent'
};
</script>

<style scoped>
/* Додайте стилі, специфічні для HeaderComponent, або залиште стилі в `style.css` */
</style>
