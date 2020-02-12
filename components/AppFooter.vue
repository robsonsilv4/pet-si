<template>
  <footer class="footer">
    <div class="container">
      <div class="columns is-multiline">
        <div class="column has-text-centered">
          <div>
            <nuxt-link to="/" class="link">Inicio</nuxt-link>
            <nuxt-link to="/blog" class="link">Blog</nuxt-link>
          </div>
        </div>
      </div>

      <div class="content is-small has-text-centered">
        <p>
          PET-SI © 2020
        </p>
      </div>
    </div>
  </footer>
</template>

<script>
export default {
  name: 'AppFooter'
}
</script>

<style></style>
