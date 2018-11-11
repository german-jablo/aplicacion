<template>
    <div id="desplegado">
      <div id="plegado" v-bind:class="{ isActive: isActive }">
        <table>
          <tr>
            <td><MenuDerecha/></td>
            <td>OCULTAR MENÚ V-SHOW</td>
          </tr>
           
          <tr>
            <td>20</td>
            <td>CSS</td>
          </tr>
           
          <tr>
            <td>20</td>
            <td>HTML</td>
          </tr>
           
          <tr>
            <td>60</td>
            <td>Dreamweaver</td>
          </tr>
          </table>
      </div>
    </div>
</template>

<script>
import MenuDerecha from './MenuDerecha'

export default {
  name: 'PlegableDerecha',
  data: function() {
    return  {
      isActive: false
    }
  },
  components: { MenuDerecha }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
  
#desplegado {
  width: 50px;
  height: 100%;
  position: absolute;
  right: 0px;
}

#plegado {
  width: 250px;
  height: 100%;
  position: absolute;
  transition-duration: 0.1s;
  box-shadow: 0 10px 20px rgba(0,0,0,0.19), 0 6px 6px rgba(0,0,0,0.23); /*si quiero quitar la sombra de abajo tendre que usar clip-path, pero como no se ve no es necesario*/

}

#plegado.isActive {
  transform: translate(-200px, 0px);
}

table { border-collapse: collapse;
  padding: 0px; margin: 0px; }

table td:nth-child(2) {
  width: 200px;
  text-align: right;
}

table td:first-child {
  width: 50px;
  text-align: center;
}

table td tr {
    vertical-align: middle;
}

tr { padding: 50px;
  margin: 50px;
  height: 50px; 
  border-bottom: solid 1px;}

</style>