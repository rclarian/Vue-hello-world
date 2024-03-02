<template>
  <h2>Fullname - {{ firstName }} {{ lastName }}</h2>
  <h2>Computed fullname - {{ fullName }}</h2>
  <h2>Inline Total - {{ items.reduce((total, curr) => (total = total + curr.price), 0) }}</h2>
  <button @click="items.push({id: 4, title: 'Keyboard', price: 50})">Add Item</button>
  <h2>Computed Total - {{ total }}</h2>

</template>

<script>

//import _ from "lodash";
export default {
  name: 'App',
  data() {
    return {
      firstName: 'Bruce',
      lastName: 'Wayne',
      items: [
        {
          id: 1,
          title: 'TV',
          price: 100,
        },
        {
          id: 2,
          title: 'Phone',
          price: 200,
        },
        {
          id: 3,
          title: 'Laptop',
          price: 300,
        },
      ],
    }
  },
  methods: {
  },
  components: {
  },
  computed: {
    fullName() {
      return `${this.firstName} ${this.lastName}`;
    },
    total() {
      return this.items.reduce((total, curr) => (total = total + curr.price), 0);
    }
  },
 
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
