<template>

  <!-- <CardComponent content="Card content 1"/>
  <CardComponent content="Card content 2"/> -->
  <CardComponent></CardComponent>
  <CardComponent>Card content</CardComponent>
  <CardComponent><h2>Card content</h2></CardComponent>
  <CardComponent>
    <img src="https://picsum.photos/200">
  </CardComponent>

  <CardComponent>
    <template v-slot:header>
      <h3>Header</h3>
    </template>
    <template v-slot:default>
      <img src="https://picsum.photos/200">
    </template>
    <template v-slot:footer>
      <button>View Details</button>
    </template>
  </CardComponent>

</template>

<script>
import CardComponent from './components/CardComponent.vue'

export default {
  name: 'App',
  components: {
    CardComponent,

  },
  data() {
    return {
      name: ''
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
