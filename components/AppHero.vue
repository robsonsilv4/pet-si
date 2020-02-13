<template>
  <section class="hero is-medium has-background is-bold is-primary">
    <img
      v-if="imgBackground"
      :src="imgBackground"
      alt=""
      class="hero-background is-transparent"
    />
    <div class="hero-body">
      <div class="container">
        <p class="title is-2">{{ title }}</p>
        <p class="subtitle is-3">{{ subtitle }}</p>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: 'AppHero',
  props: {
    title: {
      type: String,
      default: ''
    },
    subtitle: {
      type: String,
      default: ''
    },
    imgBackground: {
      type: String,
      default: ''
    }
  }
}
</script>

<style lang="scss">
.hero.has-background {
  position: relative;
  overflow: hidden;
}

.hero-background {
  position: absolute;
  object-fit: cover;
  object-position: center center;
  width: 100%;
  height: 100%;

  &.is-transparent {
    opacity: 0.3;
  }
}
</style>
