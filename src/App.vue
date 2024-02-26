<template>
  <div>{{ greet }} {{ name }}</div>
  
  <div v-html="channel"></div>
  <div v-html="hack"></div>

</template>

<script>


export default {
  name: 'App',
  data() {
    return {
      greet: "Hello",
      name: "Batman",
      channel: "<b>Codevolution</b>",
      hack: `<a href="#" onclick="alert('You have been hacked!')">Win a prize!</a>`,
    };
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
