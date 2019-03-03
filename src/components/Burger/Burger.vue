<template>
  <div>
    <BurgerIngredient type="BreadTop">
      <BurgerIngredient type="Seeds1" />
      <BurgerIngredient type="Seeds2" />
    </BurgerIngredient>

    <BurgerIngredient type="BreadBottom" />
  </div>
</template>

<script>
import BurgerIngredient from './BurgerIngredient'

export default {
  name: 'Burger',
  components: {
    BurgerIngredient
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
</style>
