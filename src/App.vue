<template>
  <!-- <img alt="Vue logo" src="./assets/logo.png"> -->

  <!-- <counter :start="1"></counter> -->
  <indecision></indecision>

</template>

<script>
import Counter from './components/Counter.vue'
import Indecision from './components/indecision.vue'



export default {
  components: { Counter, Indecision },
  name: 'App',

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
