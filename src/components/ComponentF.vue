<template>
  <h2>ComponentF</h2>
  <h3>ComponentF Username: {{ username }}</h3>
</template>

<script>

export default {
  name: 'ComponentF',
  data() {  
    return {

    }
  },
  inject: ['username']
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