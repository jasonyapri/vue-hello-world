<template>
  <img alt="Vue logo" src="./assets/logo.png">
  <h1>Slots</h1>
  <Card></Card>
  <Card>Card content</Card>
  <Card>
    <h2>Card Content</h2>
  </Card>
  <Card>
    <img src="https://picsum.photos/200" alt="Image" />
  </Card>
</template>

<script>
import Card from './components/Card_simple.vue'

export default {
  name: 'App',
  components: {
    Card,
  },
  data() {  
    return {

    }
  },
  methods: {

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

