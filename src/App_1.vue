<template>
  <img alt="Vue logo" src="./assets/logo.png">
  <div>{{ greet }} {{ name }}</div>
  <div v-html="channel"></div>
  <h2 :id="headingId">Heading</h2>
  <h2 class="underlined">Underlined text</h2>
  <h2 class="underlined" v-bind:class="status">Status</h2>
  <h2 v-bind:class="isPromoted && 'promoted'">Promoted Movie</h2>
  <button v-bind:disabled="isDisabled">Bind</button>
  <h2 :class="isSoldout ? 'sold-out' : 'new'">Soldout? movie</h2>
  <h2 :class="['new', 'promoted']">Newly promoted movie</h2>
  <h2 v-bind:class="[isPromoted && 'promoted', isSoldout ? 'sold-out' : 'new']">Array conditional movie</h2>
  <h2 v-bind:class="{
    promoted: isPromoted,
    new: !isSoldout,
    'sold-out': isSoldout
  }">Object conditional movie</h2>
  <h2 v-bind:style="{
    color: highlightColor,
    fontSize: headerSize + 'px',
    padding: '20px'
  }">Inline Style</h2>
  <h2 v-bind:style="headerStyleObject">Style Object</h2>
  <div v-bind:style="[baseStyleObject, successStyleObject]">Success Style</div>
  <div v-bind:style="[baseStyleObject, dangerStyleObject]">Danger Style</div>
</template>

<script>

export default {
  name: 'App',
  data() {  
    return {
      greet: "Hello",
      name: "Jason",
      channel: "<b>Yukbelajar Coding</b>",
      headingId: 'Heading',
      isDisabled: true,
      status: 'success',
      isPromoted: false,
      isSoldout: true,
      highlightColor: 'orange',
      headerSize: 50,
      headerStyleObject: {
        color: 'orange',
        fontSize: '50px',
        padding: '20px'
      },
      baseStyleObject: {
        fontSize: '50px',
        padding: '10px'
      },
      successStyleObject: {
        color: 'green',
        backgroundColor: 'lightgreen',
        border: '1px solid green',
        padding: '20px'
      },
      dangerStyleObject: {
        color: 'darkred',
        backgroundColor: 'red',
        border: '1px solid darkred',
        padding: '20px'
      }
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

.underlined {
  text-decoration: underline;
}

.promoted {
  font-style: Italic;
}

.new {
  color: olivedrab;
}

.sold-out {
  color: red;
}
</style>

