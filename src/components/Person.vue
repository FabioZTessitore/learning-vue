<template>
  <div class="person">
    <p @click="$emit('switch-names', 'Max!')">I'm {{name}} and I'm {{age}} years old!</p>
    <p><slot></slot></p>
    <p><input type="text" v-model="username"></p>
    <p>{{username}}</p>
  </div>
</template>

<script>
export default {
  name: 'Person',
  props: [ 'name', 'age' ],
  data: function () {
    return {
      username: ''
    };
  },
  watch: {
    username: function (newName, oldName) {
      this.$emit('switch-names', newName);
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
</style>
