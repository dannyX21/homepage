<template>
  <section id="app">
    <div class="section is-fullhd is-fluid" :class="{'is-dark': isDark, 'is-light': !isDark}">
      <Navbar @update:theme="updateTheme"></Navbar>
      <Jumbotron :is-dark="isDark"></Jumbotron>
      <img alt="Vue logo" src="./assets/logo.png">
    </div>
  </section>
</template>

<script>
import Navbar from '@/components/Navbar.vue'
import Jumbotron from '@/components/Jumbotron.vue'

export default {
  name: 'App',
  data () {
    return {
      isDark: true
    }
  },
  components: {
    Navbar,
    Jumbotron
  },
  methods: {
    updateTheme(isDark) {
      this.isDark = isDark
    }
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c363f;
}
.is-dark {
  background-color: #2c363f;
  color: #f0f0f0;

}
.is-light {
  background-color: #f0f0f0;
  color: #2c363f;
}
</style>
