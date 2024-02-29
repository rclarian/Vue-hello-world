<template>
  <!-- <h2 v-for="name in names" :key="name" v-if="name === 'Bruce'">{{ name }}</h2> -- error this type  of code--> 
  <template v-for="name of names" :key="name">
    <h2 v-if="name === 'Bruce'">{{ name }}</h2>
  </template>

</template>

<script>

//import _ from "lodash";
export default {
  name: 'App',
  data() {
    return {
      names: ['Bruce', 'Clark', 'Joanne', 'Ryan', 'Kulit'],
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
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
