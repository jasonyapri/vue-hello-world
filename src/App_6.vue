<template>
  <img alt="Vue logo" src="./assets/logo.png">
  <h1>Methods</h1>
  <h2>{{ add(2, 3, 5) }}</h2>
  <h2>{{ add(5, 10, 15) }}</h2>
  <h2>Multiply method {{ multiply(5) }}</h2>
</template>

<script>

export default {
  name: 'App',
  data() {  
    return {
      baseMultiplier: 5
    }
  },
  methods: {
    add(a, b, c) {
      return a + b + c
    },
    multiply(num) {
      return num * this.baseMultiplier
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

