<template>
  <div id="app">
    <h1>I'm a Vue App</h1>
    <button @click="switchNamesHandler">Switch Names</button>
    <Person :name="persons[0].name" :age="persons[0].age" />
    <Person :name="persons[1].name" :age="persons[1].age">My Hobbies: Racing</Person>
    <Person :name="persons[2].name" :age="persons[2].age" />
  </div>
</template>

<script>
import Person from './components/Person.vue'

export default {
  name: 'app',
  data: function () {
    return {
      persons: [
        { name: 'Max', age: 28 },
        { name: 'Manu', age: 29 },
        { name: 'Stephanie', age: 26 }
      ]
    };
  },
  methods: {
    switchNamesHandler: function () {
      console.log('clicked');
    }
  },
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
