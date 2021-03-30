<template>
    <div>
      <h2>Popup</h2>
      <input type="text" v-model="name">
      <button @click="$emit('close', name)">Close</button>
    </div>
</template>

<script>

export default {
  name: 'Popup',
  // emits: ['close'],
  emits: {
    close: (name) => {
      if (!name) {
        alert("You must enter a name!")
        return false
      } else{
        return true
      }
    }
  },
  data() {  
    return {
      name: ''
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

