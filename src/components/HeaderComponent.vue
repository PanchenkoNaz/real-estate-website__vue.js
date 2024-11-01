<template>
  <header class="header" :class="{ active: isScrolled }" data-header>
    <div class="container">
      <a href="#" class="logo">
        <img src="/src/assets/images/logo.png" width="190" height="28" alt="wealthome" />
      </a>

      <nav class="navbar" :class="{ active: isNavbarActive }" data-navbar>
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

      <button @click="toggleNavbar" class="nav-toggle-btn icon-btn" aria-label="toggle navbar" data-nav-toggler>
        <span class="material-symbols-rounded open" aria-hidden="true">menu</span>
        <span class="material-symbols-rounded close" aria-hidden="true">close</span>
      </button>
    </div>
  </header>
</template>

<script>
export default {
  name: 'HeaderComponent',
  data() {
    return {
      isNavbarActive: false, // контролює стан навігації
      isScrolled: false // контролює стан хедера при прокрутці
    };
  },
  methods: {
    toggleNavbar() {
      this.isNavbarActive = !this.isNavbarActive; // перемикає стан меню
    },
    handleScroll() {
      this.isScrolled = window.scrollY > 50; // додає/видаляє клас залежно від прокрутки
    }
  },
  mounted() {
    window.addEventListener("scroll", this.handleScroll); // додає обробник події прокрутки
  },
  beforeUnmount() {
    window.removeEventListener("scroll", this.handleScroll); // видаляє обробник перед видаленням компонента
  }
};
</script>

<style scoped>
/* Додайте стилі, щоб забезпечити коректне відображення елементів */
.header.active {
  background-color: rgba(0, 0, 0, 0.8); /* Стиль хедера при прокрутці */
}

.navbar.active {
  display: block; /* Наприклад, для мобільного меню, якщо воно приховане */
}
</style>
