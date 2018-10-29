<template>
  <div id="app">
    <PlegableDerecha/>
    <PlegableIzquierda/>
  </div>
</template>

<script>
import PlegableDerecha from './components/PlegableDerecha'
import PlegableAbajo from './components/PlegableAbajo'
import PlegableIzquierda from './components/PlegableIzquierda'

export default {
  name: 'App',
  components: {
    PlegableDerecha, PlegableAbajo, PlegableIzquierda,
  }
}
</script>

<style>
  body {
    margin: 0px;
    padding: 0px;
  }

  #app {
    overflow-x: hidden;
    background-color: pink;
    width: 100%;
    height: 100%;
    position: absolute;
  }
</style>
