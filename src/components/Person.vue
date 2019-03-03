<template>
  <div class="person">
    <p @click="$emit('switchNames', 'Max!')">I'm {{name}} and I'm {{age}} years old!</p>
    <p><slot></slot></p>
  </div>
</template>

<script>
export default {
  name: 'Person',
  props: [ 'name', 'age' ]
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
</style>
