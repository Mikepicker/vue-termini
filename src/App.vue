<template>
  <div id="app">
    <div style='width: 480px; height: 280px'>
      <Termini v-bind:commands='commands' />
    </div>
  </div>
</template>

<script>
import Home from './components/Home.vue'
import Termini from './components/Termini.vue'

export default {
  name: 'app',
  components: {
    Home,
    Termini
  },
  data: function () {
    return {
      commands: [
        'npm install @mikepicker/termini',
        'enjoy!'
      ]
    }
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
