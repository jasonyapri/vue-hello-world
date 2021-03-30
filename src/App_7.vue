<template>
  <img alt="Vue logo" src="./assets/logo.png">
  <h1>Event Handling</h1>
  <h2>{{ name }}</h2>
  <button v-on:click="changeName($event), increment($event, 1)">Change name by click</button>
  <br><br>
  <button v-on:mouseover="changeName">Change name by hover</button>

  <h2>{{ count }}</h2>
  <br><br>
  <button v-on:click="increment($event, 1)">Increment 1</button>
  <button v-on:click="decrement($event, 1)">Decrement 1</button>
  <br>
  <button v-on:click="increment($event, 5)">Increment 5</button>
  <button v-on:click="decrement($event, 5)">Decrement 5</button>
</template>

<script>

export default {
  name: 'App',
  data() {  
    return {
      name: "Jason",
      count: 0
    }
  },
  methods: {
    changeName(event) {
      this.name = "Batman"
      console.log('Event', event)
    },
    increment(event, num) {
      this.count += num
      console.log('Event', event)
    },
    decrement(event, num) {
      this.count -= num
      console.log('Event', event)
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

