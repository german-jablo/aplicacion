<template>
  <div id="root">
    <PlegableIzquierda/>
    <div id="container">
      <!--Aca va el codigo-->
    </div>
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
#root {
  width: 50%;
  height: 100%;
  float: left;
  background-color: gray;
}

#container {
  width: calc(100% - 50px);
  float: right;
  height: 100%;
}

@media screen and (min-width: 660px)  {
  #root {
  width: 40%;
  }
}
</style>
