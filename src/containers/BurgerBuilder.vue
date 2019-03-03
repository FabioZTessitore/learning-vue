<template>
  <Aux>
    <Burger />
    <div>Build Controls</div>
  </Aux>
</template>

<script>
import Aux from '../hoc/Aux';
import Burger from '../components/Burger/Burger'

export default {
  name: 'BurgerBuilder',
  components: {
    Aux,
    Burger
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
</style>
