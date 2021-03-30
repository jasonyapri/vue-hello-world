<template>
  <h2>ComponentC</h2>
  <ComponentE />
</template>

<script>
import ComponentE from './ComponentE.vue'

export default {
  name: 'ComponentC',
  components: {
    ComponentE,
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