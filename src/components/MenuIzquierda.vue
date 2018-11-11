<template>
<button class="hamburger hamburger--arrowturn"
 v-bind:class="{ isActive: isActive }"
 v-on:click="$parent.isActive = !$parent.isActive; isActive = !isActive"
 type="button">
  <span class="hamburger-box">
    <span class="hamburger-inner"></span>
  </span>
</button>
</template>

<script>

export default {
  name: 'MenuIzquierda',
  data: function() {
    return  {
      isActive: false
    }
  },
}

</script>

<!-- Add "scoped" attribute to limit CSS to this component only-->
<style scoped>
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
    -webkit-transform: translateX(11px) translateY(5.2px) rotate(45deg) scaleX(0.5);
    -ms-transform: translateX(11px) translateY(5.2px) rotate(45deg) scaleX(0.5);
    transform: translateX(11px) translateY(5.2px) rotate(45deg) scaleX(0.5);
  }
  .hamburger--arrowturn.isActive .hamburger-inner::after {
    -webkit-transform: translateX(11px) translateY(5.2px) rotate(-45deg) scaleX(0.5);
    -ms-transform: translateX(11px) translateY(5.2px) rotate(-45deg) scaleX(0.5);
    transform: translateX(11px) translateY(-5.2px) rotate(-45deg) scaleX(0.5); }
</style>
