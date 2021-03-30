<template>
    <h2>Hello {{ name }} aka {{ heroName }}</h2>
</template>

<script>
export default {
    name: "Greet",
    props: ['name', 'heroName']
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