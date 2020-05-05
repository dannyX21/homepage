<template>
  <div class="hello">
    <h1 class="is-primary">{{ msg }}</h1>
    <b-button type="is-primary" icon-left="github-circle">Button</b-button>
    
    <prism language="javascript">{{ 'const pi = 3.1415982\nconst area = r * r * pi' }}</prism>
  </div>
</template>

<script>
import 'prismjs'
import 'prismjs/themes/prism-tomorrow.css'
import Prism from 'vue-prism-component'

export default {
  name: 'HelloWorld',
  props: {
    msg: String
  },
  components: {
    Prism
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
