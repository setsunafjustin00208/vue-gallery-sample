<template>
    <nav class="navbar" role="navigation" aria-label="main navigation">
      <div class="navbar-brand">
        <a class="navbar-item" href="/">
            <img src="@/assets/images/San-andres-apostol logo-clear.png" alt="San Andres Apostol Logo" />
            <span class="navbar-title">Parokya na ning San Andres Apostol</span>
        </a>

        <a role="button" class="navbar-burger" :class="{ 'is-active': isActive }" @click="toggleNavbar" aria-label="menu" aria-expanded="false" data-target="navbarBasicExample">
          <span aria-hidden="true"></span>
          <span aria-hidden="true"></span>
          <span aria-hidden="true"></span>
          <span aria-hidden="true"></span>
        </a>
      </div>
  
      <div id="navbarBasicExample" class="navbar-menu" :class="{ 'is-active': isActive }">
        <div class="navbar-start">
          <router-link class="navbar-item" to="/">Home</router-link>
          <router-link class="navbar-item" to="/about">About</router-link>
          <router-link class="navbar-item" to="/contact">Contact</router-link>
        </div>
        <div class="navbar-end">
          <div class="navbar-item">
            <div class="buttons">
              <a class="button is-link is-rounded" href="https://www.facebook.com/SanAndresCandaba" target="_blank" aria-label="Facebook">
                <span class="icon">
                  <i class="fab fa-facebook-f"></i>
                </span>
              </a>
              <a class="button is-danger is-rounded" href="https://www.youtube.com/channel/UCXXXXXX" target="_blank" aria-label="YouTube">
                <span class="icon">
                  <i class="fab fa-youtube"></i>
                </span>
              </a>
              <a class="button is-dark is-rounded" href="https://twitter.com/SanAndresCandaba" target="_blank" aria-label="X">
                <span class="icon">
                  <i class="fab fa-twitter"></i>
                </span>
              </a>
            </div>
          </div>
        </div>
      </div>
    </nav>
  </template>
  
  <script>
  export default {
    data() {
      return {
        isActive: false
      };
    },
    methods: {
      toggleNavbar() {
        this.isActive = !this.isActive;
      }
    }
  };
  </script>
  
  <style scoped>
  .navbar-burger {
    cursor: pointer;
  }
  </style>