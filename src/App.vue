<template>
  <img alt="Vue logo" src="./assets/logo.png">
  <h1>Teleport Component</h1>
  <teleport to='#portal-root'>
    <Portal />
  </teleport>
</template>

<script>
import Portal from './components/Portal.vue'

export default {
  name: 'App',
  components: {
    Portal
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

</style>

