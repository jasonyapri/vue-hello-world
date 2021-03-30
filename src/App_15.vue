<template>
  <img alt="Vue logo" src="./assets/logo.png">
  <h1>Components, v-model and Vue.js Devtools</h1>
  <br>
  <Input v-model="name" />
</template>

<script>
import Input from './components/Input.vue'

export default {
  name: 'App',
  components: {
    Input
  },
  data() {  
    return {
      name: ''
    }
  },
  methods: {}
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

