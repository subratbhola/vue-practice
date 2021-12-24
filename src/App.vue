<template>
  <div id="app">
  <!-- //with binding -->
    <div> Hello {{name}}</div> 
    <!-- with v-text directive -->
    <div v-text="directivetext"></div> 
    <!-- <div v-html="ntmlbind"></div> -->


  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'

export default {
  name: 'App',
  components: {
    HelloWorld
  },
  data() {
    return {
      name:'Subrat',
      directivetext:'directive binding',
      ntmlbind='<b>Html Binding</b>',
      // propBinding='id1',
      // propBinding2=true
    }
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
