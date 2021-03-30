<template>
  <img alt="Vue logo" src="./assets/logo.png">
  <h1>Slot Props</h1>
  <NameList>
    <template v-slot:default="slotProps">
      {{ slotProps.firstName }} {{ slotProps.lastName }}
    </template>
  </NameList>
  <hr>
  <NameList>
    <template v-slot:default="slotProps">
      {{ slotProps.lastName }}, {{ slotProps.firstName }}
    </template>
  </NameList>
  <hr>
  <NameList>
    <template v-slot:default="slotProps">
      {{ slotProps.firstName }}
    </template>
  </NameList>
  <hr>
</template>

<script>
import NameList from './components/NameList.vue'

export default {
  name: 'App',
  data() {  
    return {

    }
  },
  components: {
    NameList
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

