<template>
  <div>
    <pre>
      {{ JSON.stringify(formValues, null, 2) }}
    </pre>
  </div>
  <form action="">
    <div>
      <label for="name">Name</label>
      <input type="text" id="name" v-model="formValues.name">
    </div>
    <div>
      <label for="profile">Profile Summary</label>
      <textarea id="profile" v-model="formValues.profileSummary"></textarea>
    </div>
    <div>
      <label for="country">Country</label>
      <select id="country" v-model="formValues.country">
        <option value="">Select a Country</option>
        <option value="India">India</option>
        <option value="Vietnam">Vietnam</option>
        <option value="Philippines">Philippines</option>
      </select>      
    </div>
    <div>
      <label for="job-location">Job Location</label>
      <select id="job-location" multiple v-model="formValues.jobLocation">
        <option value="India">India</option>
        <option value="Vietnam">Vietnam</option>
        <option value="Philippines">Philippines</option>
        <option value="Singapore">Singapore</option>
        <option value="USA">USA</option>
      </select>      
    </div>

  </form>
</template>

<script>

//import _ from "lodash";
export default {
  name: 'App',
  data() {
    return {
      formValues: {
        name: '',
        profileSummary: '',
        country: '',
        jobLocation: [],
      }
    }
  },
  methods: {
    
  },
  components: {
    
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  /* text-align: center; */
  color: #2c3e50;
  margin-top: 60px;
  
}

label {
  font-weight: bold;
  display: flex;
  margin-bottom: 5px;
  margin-top: 10px;
}

input + label {
  font-weight: bold;
  display: inline-flex;
  margin-right: 20px;
}

input[type='text'], textarea, select {
  display: block;
  width: 400px;
  padding: 6px 12px;
  font-size: 14px;
  line-height: 1.42857143;
  color: #555;
  background-color: #fff;
  background-image: none;
  border: 1px solid #ccc;
  border-radius: 6px;
}

</style>
