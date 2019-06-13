<template>
  <div id="app" :style="{backgroundColor: currentBackground}">
    <moon></moon>
    <!-- <button @click="change">Change</button> -->
  </div>
</template>

<script>
import Star from './components/Star.vue';
import Moon from './components/Moon.vue';

export default {
  name: 'app',
  data () {
    return {
      lightBackground: 'white',
      darkBackground: 'black',
      currentBackground: 'white'
    }
  },
  components: {
    'star': Star,
    'moon': Moon
  },
  methods: {
    change() {
      this.currentBackground = this.currentBackground == this.lightBackground ? this.darkBackground : this.lightBackground;
    }
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

h1, h2 {
  font-weight: normal;
}

ul {
  list-style-type: none;
  padding: 0;
}

li {
  display: inline-block;
  margin: 0 10px;
}

a {
  color: #42b983;
}
</style>
