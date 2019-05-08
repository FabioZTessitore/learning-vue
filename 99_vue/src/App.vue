<template>
  <div id="app">
    <Layout>
      <BurgerBuilder />
    </Layout>
  </div>
</template>

<script>
import Layout from './components/Layout'
import BurgerBuilder from './containers/BurgerBuilder'

export default {
  name: 'app',
  components: {
    Layout,
    BurgerBuilder
  }
}
</script>

<style>
#app {
  font-family: 'Open Sans', 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
