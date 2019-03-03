<template>
  <div id="app">
    <h1>I'm a Vue App</h1>

    <button @click="togglePersons">Toggle Persons</button>

    <div v-if="showPersons">
      <Person v-for="(person, index) in persons"
        :name="person.name"
        :age="person.age"
        :index="index"
        :key="person.id"
        @delete-person="deletePerson"
        @change-name="changeNameHandler" />
    </div>
  </div>
</template>

<script>
import Person from './components/Person.vue'

export default {
  name: 'app',
  data: function () {
    return {
      persons: [
        { id: '1', name: 'Max', age: 28 },
        { id: '2', name: 'Manu', age: 29 },
        { id: '3', name: 'Stephanie', age: 26 }
      ],
      showPersons: false
    };
  },
  methods: {
    changeNameHandler: function (newName, id) {
      const person = this.persons.find(person => {
        return id === person.id;
      });
      person.name = newName;
    },
    togglePersons: function () {
      this.showPersons = !this.showPersons;
    },
    deletePerson: function (personIndex) {
      this.persons.splice(personIndex, 1);
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

button {
  backgroundColor: white;
  font: inherit;
  border: 1px solid blue;
  padding: 8px;
  cursor: pointer;
}
</style>
