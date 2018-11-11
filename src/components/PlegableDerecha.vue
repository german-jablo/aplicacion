<template>
  <div class="outer-div" v-bind:class="{ isActive: isActive }">
    <table>
      <tr>
        <td><MenuDerecha/></td>
        <td>Sección</td>
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
  
.outer-div {
  width:50px;
  height: 100%;
  float: right;
  box-shadow: 0 10px 20px rgba(0,0,0,0.19), 0 6px 6px rgba(0,0,0,0.23);
  transition-duration: 0.1s; 
  background-color: transparent;
}

.outer-div.isActive {
  width: 250px;
}

table { 
  float: left; 
  border-collapse: collapse;
}

table td:nth-child(1) {
  width: 48px;
  min-width: 48px;
  text-align: center;
  border-left: transparent 1px solid;
}

table td:nth-child(2) {
  width: 200px;
}

tr { 
  border-bottom: solid 1px;
  height: 50px;
}

</style>