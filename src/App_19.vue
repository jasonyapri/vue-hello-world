<template>
  <img alt="Vue logo" src="./assets/logo.png">
  <h1>Component Styles</h1>
  <h4>App Component Text</h4>
  <ChildStyles>
    <h4>ChildStyles Component Tag</h4>
  </ChildStyles>
</template>

<script>
import ChildStyles from './components/ChildStyles.vue'

export default {
  name: 'App',
  components: {
    ChildStyles
  },
  data() {  
    return {

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
  color: #2c3e50;
  margin-top: 60px;
}

h4 {
  color: orange;
}
</style>

