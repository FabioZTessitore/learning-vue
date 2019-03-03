<template>
  <div class="person">
    <p>I'm {{name}} and I'm {{age}} years old!</p>
  </div>
</template>

<script>
export default {
  name: 'Person',
  data: function () {
    return {
      name: 'Max'
    }
  },
  computed: {
    age: function () {
      return Math.floor(Math.random()*30);
    }
  },
  props: {
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
</style>
