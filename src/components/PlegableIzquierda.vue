<template>
    <div id="desplegado">
      <div id="plegado" v-bind:class="{ isActive: isActive }">
        <table>
          <tr>
            <td>Sección</td>
            <td><MenuIzquierda/></td>
          </tr>
           
          <tr>
            <td>CSS</td>
            <td>20</td>
          </tr>
           
          <tr>
            <td>HTML</td>
            <td>20</td>
          </tr>
           
          <tr>
            <td>Dreamweaver</td>
            <td>60</td>
          </tr>
          </table>
      </div>
    </div>
</template>

<script>
import MenuIzquierda from './MenuIzquierda'

export default {
  name: 'PlegableIzquierda',
  data: function() {
    return  {
      isActive: false
    }
  },
  components: { MenuIzquierda }
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
  width: 250px;
  height: 100%;
  position: absolute;
  right: 0;
  align-content: right;
  transition-duration: 0.1s;
  box-shadow: 0 10px 20px rgba(0,0,0,0.19), 0 6px 6px rgba(0,0,0,0.23); /*si quiero quitar la sombra de abajo tendre que usar clip-path, pero como no se ve no es necesario*/
}

#plegado.isActive {
  transform: translate( 200px, 0px);
}

table { border-collapse: collapse;
  padding: 0px; margin: 0px; }

table td:nth-child(2) {
  width: 50px;
  text-align: center;
}

table td:first-child {
  width: 200px;
}

table td tr {
    vertical-align: middle;
}

tr { padding: 50px;
  margin: 50px;
  height: 50px; 
  border-bottom: solid 1px;}


</style>