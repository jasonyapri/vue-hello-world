<template>
  <img alt="Vue logo" src="./assets/logo.png">
  <h1>Components, Prop Types and Validations</h1>
  <!-- <Greet name="Bruce" heroName="Batman"/>
  <Greet name="Clark" hero-name="Superman"/>
  <Greet name="Diana" heroName="Wonder Woman"/>
  <Greet :name="name" :hero-name="store"/> -->
  <Article id="my-article" title="Article Title" :likes="50" :isPublished="true"/>
</template>

<script>
// import Greet from './components/Greet.vue'
import Article from './components/Article.vue'

export default {
  name: 'App',
  components: {
    // Greet,
    Article
  },
  data() {  
    return {
      name: 'Jason',
      store: 'Yupmart'
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

