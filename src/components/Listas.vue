<template>
  <div>
    <PlegableIzquierda/>
  </div>
</template>

<script>


import PlegableIzquierda from './PlegableIzquierda'

export default {
  name: 'Listas',
  components: { PlegableIzquierda }
  }
</script>

<!-- Add "scoped" attribute to limit CSS to this component only-->
<style scoped>
div {
  width: 50%;
  height: 100%;
  background-color: yellow;
  float: left;
}

@media screen and (min-width: 660px)  {
  div {
  width: 40%;
  }
}
</style>
