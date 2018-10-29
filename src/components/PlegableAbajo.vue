<template>
    <div id="desplegado">
      <div id="plegado"></div>
    </div>
</template>

<script>
export default {
  name: 'PlegableAbajo',
  }
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
  
  #desplegado {
  width: 100%;
  height: 50px;
  bottom: 0px;
  clip-path: inset(-10000px -10000px 0px -10000px);
  position: absolute;

  background-color: blue;
}

#plegado {
  width: 100%;
  height: 300px;
  right: 0;
  align-content: right;
  transition-duration: 0.1s;
 
  background-color: orange;
}

#plegado:hover{
  transform: translate(0px, -250px);
}
</style>
