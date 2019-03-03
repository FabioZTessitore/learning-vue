<template>
  <div class="person">
    <div @click="$emit('delete-person', index)">
      <p>I'm {{name}} and I'm {{age}} years old!</p>
      <p><slot></slot></p>
      <p>{{username}}</p>
    </div>
    <p><input type="text" v-model="username"></p>
  </div>
</template>

<script>
export default {
  name: 'Person',
  props: [ 'name', 'age', 'index' ],
  data: function () {
    return {
      username: this.name
    };
  },
  watch: {
    username: function (newName, oldName) {
      this.$emit('switch-name', newName, this.$vnode.key);
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.person {
  width: 60%;
  margin: 2em auto;
  border: 1px solid #eee;
  box-shadow: 0 2px 3px #aaa;
  padding: 16px;
  text-align: center;
}
</style>
