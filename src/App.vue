<template>
  <h2>{{ name }}</h2>
  <div>
    <button @click="changeName($event), increment(1, $event)">Change name</button>
    <button @mouseover="name = 'Mouse'">Mouseover Change name</button>
    <button @mouseover="name = 'Vishwas'">Original name</button>
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
    <button @click="increment(1, $event)">Increment 1</button>
    <button @click="increment(5, $event)">Increment 5</button>
    <button @click="decrement(1)">Decrement 1</button>
    <button @click="decrement(5)">Decrement 5</button>
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
    increment(num, event){
      this.count += num;
      console.log('Event', event);
    },
    decrement(num){
      this.count -= num;
    },
    changeName(event){
      this.name = 'Batman';
      console.log('Event', event);
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
