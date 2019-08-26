<template>
  <div id="app">
    <SmartAddress/>
  </div>
</template>

<script>
import SmartAddress from './components/SmartAddress.vue'

export default {
  name: 'app',
  components: {
    SmartAddress
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
