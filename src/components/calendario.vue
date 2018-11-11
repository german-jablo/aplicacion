<template>
  <div>
    <PlegableDerecha/>
  </div>
</template>

<script>


import PlegableDerecha from './PlegableDerecha'

export default {
  name: 'Calendario',
  components: { PlegableDerecha }
  }
</script>

<!-- Add "scoped" attribute to limit CSS to this component only-->
<style scoped>
div {
  width: 50%;
  height: 100%;
  float: left;
  background-color: yellow;
}

@media screen and (min-width: 660px)  {
  div {
  width: 60%;
}
}
</style>
