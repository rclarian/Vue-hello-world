<template>
  <div>
    <GreetComponent name="Ryan" hero-name="Batman"/>
    <GreetComponent name="Clark" hero-name="Superman"/>
    <GreetComponent name="Diana" hero-name="Wonder Woman"/>
    <GreetComponent :name="name" :hero-name="channel"/>

    <ArticleComponent title="Article Title by Ryan" :likes="50" :isPublished="false"/>
    <ArticleComponent :likes="50" :isPublished="false"/>
    
    
  </div>
</template>

<script>
import GreetComponent from './components/GreetComponent.vue'
import ArticleComponent from './components/ArticleComponent.vue'

export default {
  name: 'App',
  components: {
    GreetComponent,
    ArticleComponent
  },
  data() {
    return {
      name: 'Vishwas',
      channel: 'Codevolution',
    }
  },
  methods: {},
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
