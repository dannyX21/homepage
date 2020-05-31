<template>
  <b-navbar :type="isDark ? 'is-dark': 'is-light'" :spaced="true" :fixed-top="true">
    <template slot="start">
      <b-navbar-item href="#">
        <b-icon icon="home" size="is-large" type="is-primary"></b-icon>
      </b-navbar-item>
    </template>
    <template slot="end">
      <b-navbar-item tag="div">
        <div class="buttons">
          <a class="button" :class="isDark ? 'is-dark' : 'is-light'" @click="toggleDark">
            <b-icon icon="theme-light-dark" size="is-small"></b-icon>
          </a>
        </div>
      </b-navbar-item>
    </template>
  </b-navbar>
</template>
<script>
export default {
  data () {
    return {
      isDark: true
    }
  },
  methods: {
    toggleDark () {
      this.isDark = !this.isDark
      this.$emit('update:theme', this.isDark)
    }
  }
}
</script>