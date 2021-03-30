<template>
  <img alt="Vue logo" src="./assets/logo.png">
  <h1>Provide and Inject</h1>
  <h3>AppComponent Username: {{ username }}</h3>
  <ComponentC />
</template>

<script>
import ComponentC from './components/ComponentC.vue'

export default {
  name: 'App',
  components: {
    ComponentC,
  },
  data() {  
    return {
      username: 'jasonyapri'
    }
  },
  provide() {
    return {
      username: this.username
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

</style>