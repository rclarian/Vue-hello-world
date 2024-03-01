<template>
  <h2>{{ name }}</h2>
  <div>
    <button v-on:click="name = 'Batman'">Change name</button>
    <button v-on:mouseover="name = 'Mouse'">Mouseover Change name</button>
    <button v-on:mouseover="name = 'Vishwas'">Original name</button>
  </div>

  <h2>{{ count }}</h2>
  <div>
    <h3>Inline</h3>
    <button v-on:click="count += 1">Increment</button>
    <button v-on:click="count -= 1">Decrement</button>
  </div>
  <br>
  <div>
    <h3>Method</h3>
    <button v-on:click="increment(1)">Increment 1</button>
    <button v-on:click="increment(5)">Increment 5</button>
    <button v-on:click="decrement(1)">Decrement 1</button>
    <button v-on:click="decrement(5)">Decrement 5</button>
  </div>

</template>

<script>

//import _ from "lodash";
export default {
  name: 'App',
  data() {
    return {
      name: 'Vishwas',
      count: 0
    }
  },
  methods: {
    increment(num){
      return this.count += num;
    },
    decrement(num){
      return this.count -= num;
    },
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
