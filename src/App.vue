<template>
  <template v-for="name in names" :key="name">
    <h2>{{ name }}</h2>
    <input type="text" placeholder="Last name">
    <hr />
  </template>
  <button @click="shuffle">Shuffle!</button>

</template>

<script>

import _ from "lodash";
export default {
  name: 'App',
  data() {
    return {
      names: ['Bruce', 'Clark', 'Joanne', 'Ryan', 'Kulit'],
    }
  },
  methods: {
    shuffle() {
      console.log(this.names);
      this.names = _.shuffle(this.names);
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
