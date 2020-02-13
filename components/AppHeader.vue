<template>
  <nav class="navbar is-primary">
    <div class="container">
      <div class="navbar-brand">
        <a href="/" class="navbar-item">PET-SI</a>
        <a
          role="button"
          class="navbar-burger burger"
          aria-label="menu"
          aria-expanded="false"
          :class="{ 'is-active': showNav }"
          @click="showNav = !showNav"
        >
          <span aria-hidden="true"></span>
          <span aria-hidden="true"></span>
          <span aria-hidden="true"></span>
        </a>
      </div>
      <div class="navbar-menu" :class="{ 'is-active': showNav }">
        <div class="navbar-start">
          <nuxt-link to="/" exact class="navbar-item">Inicio</nuxt-link>
          <nuxt-link to="/blog" exact class="navbar-item">Blog</nuxt-link>
        </div>
      </div>
    </div>
  </nav>
</template>

<script>
export default {
  name: 'AppHeader',
  data() {
    return {
      showNav: false
    }
  }
}
</script>

<style></style>
