<template>
  <div>
    <h1>Home</h1>
    <p>{{ count }}</p>
    <button @click='increment'>+</button>
    <button @click='decrement'>-</button>
  </div>
</template>

<script>
import { mapState, mapMutations } from 'vuex'

export default {
  name: 'Home',
  data: () => (
    {todos: [{text: 'do this', id: 0}, {text: 'do that', id: 1}]}
  ),
  computed: mapState(['count']),
  methods: mapMutations([
    'increment',
    'decrement'
  ])
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h1 {
  color: red;
}
</style>
