<template>
  <div id='container'>
    <div id='top'>
      <div id='btn-container'>
        <div class='btn red'></div>
        <div class='btn yellow'></div>
        <div class='btn green'></div>
      </div>
    </div>

    <div id='body'>
      <div class='wrapper' v-bind:key='index' v-for='(command, index) in commands'>
        <p><span class='shell'>> </span>{{ command }}<span class='caret' v-bind:style='{"animation-delay": index * 2 + "s"}'>&nbsp;</span></p>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Termini',
  props: ['commands']
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
#container {
  position: relative;
  border-radius: 5px;
  overflow: hidden;
  width: 100%;
  height: 100%;
}

#top {
  width: 100%;
  height: 32px;
  background-color: #1d2130;
  display: flex;
  flex-direction: column;
  justify-content: center;
}

.btn {
  float: left;
  background: #f00;
  width: 10px;
  height: 10px;
  border-radius: 50%;
  margin-left: 8px;
}

.red {
  background: #d0021b;
}

.yellow {
  background: #f5a623;
}

.green {
  background: #7ed321;
}

#body {
  width: 100%;
  height: 100%;
  background-color: #272b39;
  padding: 0px 8px;
}

.shell {
  color: #4c535c;
}

p {
  position: relative;
	color: #fff;
	font-family: 'Inconsolata', Consolas, monospace;
	font-size: 12px;
  margin: 0;
  padding-top: 8px;
}

p .caret {
	position: absolute;
	top: 0;
	right: 0;
	background: #272b39;
	width: 100%;
  padding-top: 8px;
  animation: typing 3s forwards;
}

@-webkit-keyframes typing{
	from { width: 100%;}
	to { width: 0;}
}

@-webkit-keyframes cursor{
	50% { border-color: white;}
}

p .caret-2 {
  animation-delay: 3s;
}

</style>
