# vue-termini: no-javascript animated terminal frame for Vue.js

![termini](termini.gif)

## Project setup
```
npm install vue-termini
```

Then, import Termini component:
```
<template>
  <div>
    <div style='width: 480px; height: 280px'>
      <Termini v-bind:commands='commands' />
    </div>
  </div>
</template>

<script>
import Termini from 'vue-termini'

export default {
  name: 'HelloWorld',
  data: function () {
    return {
      commands: [
        'npm install vue-termini',
        'enjoy!'
      ]
    }
  },
  components: {
    Termini
  }
</script>
```
