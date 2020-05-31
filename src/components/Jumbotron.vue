<template>
  <div class="columns">
    <div class="column is-one-third">
      <div class="hero" :class="isDark ? 'is-dark' : 'is-light'">
        <div class="columns">
          <div class="column is-2">
          </div>
          <div class="column is-three-quarters">
            <div class="box has-background-primary is-bold is-flex is-horizontal-centered">
              <figure class="image is-128x128">
                <img class="is-rounded" src="photo.jpg" alt="Danny">
              </figure>
            </div>
            <p class="title">Daniel Lopez M.</p>
            <p class="subtitle"><a href="mailto:dlopez@revcascade.com">dlopez@revcascade.com</a></p>
          </div>
        </div>
      </div>
    </div>
    <div class="column is-two-thirds">
      <div class="hero is-medium is-bold" :class="isDark ? 'is-dark' : 'is-light'">
        <div class="hero-body">
          <div class="container">
            <h1 class="title">
              Hi, I'm Danny Lopez
            </h1>
            <h2 class="subtitle">
              Software Developer
            </h2>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>
<script>
export default {
  data () {
    return {
    }
  },
  props: {
    isDark: {
      type: Boolean,
      default: true
    }
  }
}
</script>
<style scoped>
.is-horizontal-centered {
  justify-content: center;
}
</style>