<template>
  <h2>{{ 2 + 3 + 5 }}</h2>
  <h2>{{ 5 + 10 + 15 }}</h2>
  <h2>Add method - {{ add(6, 34, 10) }}</h2>
  <h2>Add method - {{ add(100, 340, 110) }}</h2>
  <h2>Sub method - {{ sub(340, 100, 110) }}</h2>
  <h2>Multiply method - {{ multiply(baseValue) }}</h2>

</template>

<script>

//import _ from "lodash";
export default {
  name: 'App',
  data() {
    return {
      baseMultiplier: 5,
      baseValue: 2
    }
  },
  methods: {
    add(a, b, c) {
      return a + b + c;
    },
    sub(a, b, c) {
      return a - b - c;
    },
    multiply(num){
      return num * this.baseMultiplier;
    }
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
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
  
}
</style>
