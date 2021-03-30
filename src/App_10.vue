<template>
  <img alt="Vue logo" src="./assets/logo.png">
  <h1>Computer Properties & Methods & v-for & Computed Setter</h1>
  <h2>Fullname: {{ firstName }} {{ lastName }}</h2>
  <h2>Computed Fullname: {{ fullName }}</h2>
  <br>
  <button @click="changeFullName()">Change Full Name</button>
  <hr>
  <h2>Total: {{ items.reduce((total, curr) => total = (total + curr.price), 0) }}</h2>
  <button @click="items.push({id: 4, title: 'Keyboard', price: 50})">Add item</button>
  <h2>Computed Total: {{ total }}</h2>
  <h2>Method Total: {{ getTotal() }}</h2>
  <hr>
  Country <input type="text" v-model="country">
  <hr>
  <template v-for="item in items" :key="item.id">
    <h2 v-if="item.price > 100">{{ item.title }} - {{ item.price }}</h2>
  </template>
  <hr>
  <h2 v-for="item in expensiveItems" :key="item.id">
    {{ item.title }} - {{ item.price }}
  </h2>
</template>

<script>

export default {
  name: 'App',
  data() {  
    return {
      firstName: 'Jason',
      lastName: 'Yapri',
      items: [
        {
          id: 1,
          title: 'TV',
          price: 100
        },
        {
          id: 2,
          title: 'Phone',
          price: 200
        },
        {
          id: 3,
          title: 'Laptop',
          price: 300
        }
      ],
      country: ''
    }
  },
  methods: {
    getTotal() {
      console.log('getTotal method')
      return this.items.reduce((total, curr) => total = (total + curr.price), 0)
    },
    changeFullName() {
      this.fullName = 'Clark Kent'
    }
  },
  computed: {
    fullName: {
      get() {
        return `${this.firstName} ${this.lastName}`
      },
      set(values) {
        const names = values.split(' ')
        this.firstName = names[0]
        this.lastName = names[1]
      }
    },
    total() {
      console.log('totala computed property')
      return this.items.reduce((total, curr) => total = (total + curr.price), 0)
    },
    expensiveItems() {
      return this.items.filter(item => item.price > 100)
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

