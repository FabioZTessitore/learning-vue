<template>
  <Aux>
    <div>Toolbar, SideDrawer, Backdrop</div>
    <main>
      <slot></slot>
    </main>
  </Aux>
</template>

<script>
import Aux from '../hoc/Aux';

export default {
  name: 'Layout',
  components: {
    Aux
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
</style>
