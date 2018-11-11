<template>
    <div id="desplegado">
      <div id="plegado" v-bind:class="{ isActive: isActive }">
        <table>
          <tr>
            <td>Sección</td>
            <td>
              <button class="hamburger hamburger--arrowturn"
                v-bind:class="{ isActive: isActive }"
                v-on:click="isActive = !isActive"
                type="button">
                <span class="hamburger-box">
                  <span class="hamburger-inner"></span>
                </span>
              </button>
            </td>
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

export default {
  name: 'PlegableIzquierda',
  data: function() {
    return  {
      isActive: false
    }
  },
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

button:focus {outline:0;}

.hamburger {
  padding: 3px 3px;
  display: inline-block;
  cursor: pointer;
  transition-property: opacity, filter;
  transition-duration: 0.15s;
  transition-timing-function: linear;
  font: inherit;
  text-transform: none;
  background-color: transparent;
  border: 0;
  margin: 0;
  overflow: visible; }
  .hamburger:hover {
    opacity: 0.7; }
  .hamburger.isActive:hover {
    opacity: 0.7; }
  .hamburger.isActive .hamburger-inner,
  .hamburger.isActive .hamburger-inner::before,
  .hamburger.isActive .hamburger-inner::after {
    background-color: #000; }

.hamburger-box {
  width: 35px; /*ancho del span donde está contenida la hamburgesa*/
  height: 24px; /*alto del span donde está contenida la hamburgesa*/
  display: inline-block;
  position: relative;
}

.hamburger-inner {
  display: block;
  top: 50%;
  margin-top: -2px; }
  .hamburger-inner, .hamburger-inner::before, .hamburger-inner::after {
    width: 35px; /*ancho de la hamburgesa. Si se cambia hay que retocar la traslacion*/
    height: 4px; /*alto de las 3 lineas de las hamburguesas*/
    background-color: #000;
    border-radius: 4px;
    position: absolute;
    transition-property: transform;
    transition-duration: 0.15s;
    transition-timing-function: ease; }
  .hamburger-inner::before, .hamburger-inner::after {
    content: "";
    display: block; }
  .hamburger-inner::before {
    top: -10px; }
  .hamburger-inner::after {
    bottom: -10px; }

/* Arrow Turn */
.hamburger--arrowturn.isActive .hamburger-inner {
  transform: rotate(-180deg); }
  .hamburger--arrowturn.isActive .hamburger-inner::before {
    -webkit-transform: translateX(22px) translateY(3px) rotate(45deg);
    -ms-transform: translateX(22px) translateY(3px) rotate(45deg);
    transform: translateX(11px) translateY(5.2px) rotate(45deg) scaleX(0.5);
  }
  .hamburger--arrowturn.isActive .hamburger-inner::after {
    -webkit-transform: translateX(22px) translateY(3px) rotate(45deg);
    -ms-transform: translateX(22px) translateY(3px) rotate(45deg);
    transform: translateX(11px) translateY(-5.2px) rotate(-45deg) scaleX(0.5); }
</style>