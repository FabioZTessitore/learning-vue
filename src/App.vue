<template>
  <div id="app">
    <h1>I'm a Vue App</h1>
    <Person name="Max" age="28" />
    <Person name="Manu" age="29">My Hobbies: Racing</Person>
    <Person name="Stephanie" age="26" />
  </div>
</template>

<script>
import Person from './components/Person.vue'

export default {
  name: 'app',
  components: {
    Person
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
