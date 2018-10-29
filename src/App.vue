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
    PlegableDerecha, PlegableAbajo, PlegableIzquierda
  }
}
</script>

<style>
#app {
  padding-left: 50px;
  padding-right: 50px;
  width: 400px;
  height: 450px;
  position: absolute;
  left: 200px;
  top: 100px;
  background-color: pink;
}
</style>
