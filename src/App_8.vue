<template>
  <img alt="Vue logo" src="./assets/logo.png">
  <h1>Form Handling & Modifiers</h1>
  <div>
    <pre>{{ JSON.stringify(formValues, null, 2) }}</pre>
  </div>
  <form @submit.prevent="submitForm">
    <div>
      <label for="name">Name</label> 
      <input type="text" id="name" v-model.trim.lazy="formValues.name">
    </div>
    <br />
    <div>
      <label for="profile">Profile Summary</label> 
      <textarea id="profile" cols="30" rows="10" v-model="formValues.profileSummary"></textarea>
    </div>
    <br />
    <div>
      <label for="country">Country</label>
      <select id="country" v-model="formValues.country">
        <option value="">Select a country</option>
        <option value="indonesia">Indonesia</option>
        <option value="singapore">Singapore</option>
        <option value="malaysia">Malaysia</option>
      </select>
    </div>
    <br />
    <div>
      <label for="job-location">Job Location</label>
      <select id="job-location" multiple v-model="formValues.jobLocation">
        <option value="indonesia">Indonesia</option>
        <option value="singapore">Singapore</option>
        <option value="malaysia">Malaysia</option>
      </select>
    </div>
    <br />
    <div>
      <input type="checkbox" id="remoteWork" v-model="formValues.remoteWork" true-value="yes" false-value="no">
      <label for="remoteWork">Open to remote work?</label>
    </div>
    <br />
    <div>
      <label>Skill Set</label>
      <input type="checkbox" id="html" value="html" v-model="formValues.skillset" />
      <label for="html">HTML</label>
      <input type="checkbox" id="css" value="css" v-model="formValues.skillset" />
      <label for="css">CSS</label>
      <input type="checkbox" id="javascript" value="javascript" v-model="formValues.skillset" />
      <label for="javascript">Javascript</label>
    </div>
    <br />
    <div>
      <label>Years of Experienece</label>
      <input type="radio" id="0-2" value="0-2" v-model="formValues.yearsOfExperience">
      <label for="0-2">0-2</label>
      <input type="radio" id="3-5" value="3-5" v-model="formValues.yearsOfExperience">
      <label for="3-5">3-5</label>
      <input type="radio" id="6-10" value="6-10" v-model="formValues.yearsOfExperience">
      <label for="6-10">6-10</label>
      <input type="radio" id="10+" value="10+" v-model="formValues.yearsOfExperience">
      <label for="10+">10+</label>
    </div>
    <br />
    <div>
      <label for="age">Age</label>
      <input @keyup.enter="submitForm" type="number" id="age" v-model="formValues.age">
    </div>
    <br />
    <!-- <div>
      <button>Submit</button>
    </div> -->
  </form>
</template>

<script>

export default {
  name: 'App',
  data() {  
    return {
      formValues: {
        name: '',
        profileSummary: '',
        country: '',
        jobLocation: [],
        remoteWork: "no",
        skillset: [],
        yearsOfExperience: '',
        age: null
      }
    }
  }, methods: {
  submitForm(event) {
    event.preventDefault();
    console.log('Form values', this.formValues)
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

