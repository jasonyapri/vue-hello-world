<template>
  <h2>ComponentE</h2>
  <ComponentF />
</template>

<script>
import ComponentF from './ComponentF.vue'

export default {
  name: 'ComponentE',
  components: {
    ComponentF,
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