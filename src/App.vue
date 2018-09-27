<template>
  <div id="app">
    <input v-model="name" /><br>
  <span>
     <qr-code v-bind:text="name">
    Show this if the rendering fails.
  </qr-code>
  </span>
<br>
  <span> {{name}} </span>
<br>
    <img alt="Vue logo" src="./assets/logo.png">
    
    <HelloWorld msg="Welcome to Your Vue.js App"/>
  </div>
</template>

<script>
//import HelloWorld from './components/HelloWorld.vue'
import VueQRCodeComponent from 'vue-qrcode-component'

export default {
  name: 'app',
  components: {
    'qr-code': VueQRCodeComponent
   // HelloWorld,
  },
   data() {
    return {
      name: 'test',
    }
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
