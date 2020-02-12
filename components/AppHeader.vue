<template>
  <nav class="navbar is-info">
    <div class="container">
      <div class="navbar-brand">
        <a href="/" class="navbar-item">PET-SI</a>
        <a
          role="button"
          class="navbar-burger burger"
          aria-label="menu"
          aria-expanded="false"
          data-target="navMenu"
        >
          <span aria-hidden="true"></span>
          <span aria-hidden="true"></span>
          <span aria-hidden="true"></span>
        </a>
      </div>
      <div id="navMenu" class="navbar-menu">
        <div class="navbar-start">
          <nuxt-link to="/" class="navbar-item">Inicio</nuxt-link>
          <nuxt-link to="/blog" class="navbar-item">Blog</nuxt-link>
        </div>
      </div>
    </div>
  </nav>
</template>

<script>
export default {
  name: 'AppHeader'
}
</script>

<style></style>
