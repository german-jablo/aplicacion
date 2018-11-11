<template>
  <div id="root">
    <PlegableDerecha/>
    <div id="container">
      <!--Aca va el codigo-->
    </div>
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
#root {
  width: 50%;
  height: 100%;
  float: left;
  background-color: yellow;
}

#container {
  width: calc(100% - 50px);
  float: right;
  height: 100%;
}

@media screen and (min-width: 660px)  {
  #root {
  width: 60%;
}
}
</style>
