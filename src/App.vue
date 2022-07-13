<template>
  <div id="app">
    <ExamenPractico />
  </div>
</template>

<script>
import ExamenPractico from './componentes/ExamenPractico.vue';


export default {
  name: 'App',
  components: {
    ExamenPractico,
}
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
