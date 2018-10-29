<template>
    <div id="desplegado">
      <div id="plegado"></div>
    </div>
</template>

<script>
export default {
  name: 'PlegableIzquierda',
  }
</script>

<!-- Add "scoped" attribute to limit CSS to this component only-->
<style scoped>
  
#desplegado {
  width: 50px;
  height: 100%;
  position: absolute;
  left:0px;
}

#plegado {
  width: 300px;
  height: 100%;
  position: absolute;
  right: 0;
  align-content: right;
  transition-duration: 0.1s;
  box-shadow: 0 10px 20px rgba(0,0,0,0.19), 0 6px 6px rgba(0,0,0,0.23); /*si quiero quitar la sombra de abajo tendre que usar clip-path, pero como no se ve no es necesario*/

}

#plegado:hover{
  transform: translate(250px, 0px);
}
</style>
