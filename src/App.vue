<template>
  <button @click="showPopup = true">Show Popup</button>
  <!-- <PopupComponent v-show="showPopup" @close="showPopup = false"/> -->
  <PopupComponent v-show="showPopup" @close="closePopup"/>
</template>

<script>

import PopupComponent from './components/PopupComponent.vue';

export default {
  name: 'App',
  components: {
    PopupComponent,

  },
  data() {
    return {
      showPopup: false
    }
  },
  provide() {
    return {  
    }
  },
  methods: {
    closePopup(name) {
      this.showPopup = false
      console.log('name', name)
    }
  },
  computed: {},
  watch: {},
  
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
