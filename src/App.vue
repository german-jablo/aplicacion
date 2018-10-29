<template>
  <div id="app">
    <Listas/>
    <Calendario/>
  </div>
</template>

<script>
import PlegableDerecha from './components/PlegableDerecha'
import PlegableAbajo from './components/PlegableAbajo'
import PlegableIzquierda from './components/PlegableIzquierda'
import Listas from './components/Listas'
import Calendario from './components/Calendario'

export default {
  name: 'App',
  components: {
    PlegableDerecha, PlegableAbajo, PlegableIzquierda, Listas, Calendario
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
    width: 200%;
    height: 100%;
    position: absolute;
  }
</style>
