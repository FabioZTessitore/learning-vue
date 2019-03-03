<template>
  <div :class="type">
    <slot></slot>
  </div>
</template>

<script>
export default {
  name: 'BurgerIngredient',
  props: {
    type: {
      type: String,
      required: true
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
div {
  padding: 20px;
}

.BreadTop {
  height: 20%;
  width: 80%;
  background: linear-gradient(#bc581e, #e27b36);
  border-radius: 50% 50% 0 0;
  box-shadow: inset -15px 0 #c15711;
  margin: 2% auto;
  position: relative;
}

.BreadBottom {
  height: 13%;
  width: 80%;
  background: linear-gradient(#f08e4a, #e27b36);
  border-radius: 0 0 30px 30px;
  box-shadow: inset -15px 0 #c15711;
  margin: 2% auto;
  position: relative;
}

.Seeds1 {
  width: 1%;
  height: 2%;
  position: absolute;
  background-color: white;
  left: 30%;
  top: 50%;
  border-radius: 40%;
  transform: rotate(-20deg);
  box-shadow: inset -2px -3px #c9c9c9;
}

.Seeds1:after {
  content: "";
  width: 100%;
  height: 100%;
  position: absolute;
  background-color: white;
  left: -170%;
  top: -260%;
  border-radius: 40%;
  transform: rotate(60deg);
  box-shadow: inset -1px 2px #c9c9c9;
}

.Seeds1:before {
  content: "";
  width: 100%;
  height: 100%;
  position: absolute;
  background-color: white;
  left: 180%;
  top: -50%;
  border-radius: 40%;
  transform: rotate(60deg);
  box-shadow: inset -1px -3px #c9c9c9;
}

.Seeds2 {
  width: 1%;
  height: 1%;
  position: absolute;
  background-color: white;
  left: 64%;
  top: 50%;
  border-radius: 40%;
  transform: rotate(10deg);
  box-shadow: inset -3px 0 #c9c9c9;
}

.Seeds2:before {
  content: "";
  width: 100%;
  height: 100%;
  position: absolute;
  background-color: white;
  left: 150%;
  top: -130%;
  border-radius: 40%;
  transform: rotate(90deg);
  box-shadow: inset 1px 3px #c9c9c9;
}

.Meat {

}
</style>
