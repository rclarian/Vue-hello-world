<template>
  <teleport to="#portal-root">
    <PortalComponent />
  </teleport>
 

</template>

<script>
import PortalComponent from './components/PortalComponent.vue'

export default {
  name: 'App',
  components: {
    PortalComponent,
  },
  data() {
    return {
      activeTab: 'TabA'
    }
  },
  provide() {
    return { 
      
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
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
