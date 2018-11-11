<template>
    <div class="outer-div" v-bind:class="{ isActive: isActive }">
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
  
.outer-div {
  width:50px;
  height: 100%;
  position: absolute;
  box-shadow: 0 10px 20px rgba(0,0,0,0.19), 0 6px 6px rgba(0,0,0,0.23);
  transition-duration: 0.1s; 
  background-color: transparent;
}

.outer-div.isActive {
  width: 250px;
}

table { 
  float: right; 
  border-collapse: collapse;
}

table td:nth-child(2) {
  width: 48px;
  min-width: 48px;
  text-align: center;
  border-left: transparent 1px solid;
}

table td:nth-child(1) {
  width: 200px;
}

tr { 
  border-bottom: solid 1px;
  height: 50px;
}

</style>