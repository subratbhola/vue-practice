<template>
  <div id="app">
  <!-- //with binding -->
    <div> Hello {{name}}</div> 
    <!-- with v-text directive -->
    <div v-text="directivetext"></div> 
    <div v-html="ntmlbind"></div>
    <button v-bind:id="propBinding" v-bind:disabled="propBinding2">Submit</button>

    <!-- class binding -->
    <h2 v-bind:class="'red'">class red</h2>
    <h2 v-bind:class="isSoldout ? 'red':'green'">conditional class</h2>
    <p v-bind:class="['red','italic']">array of class bind</p>
    <p v-bind:class="{red:isSoldout}">object of class bind</p>
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
      ntmlbind:'<b>Html Binding</b>',
      propBinding:'id1',
      propBinding2:true,
      isSoldout:true
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

.red {
  color:red;
}

.green {
  color: green;
}

.italic {
  font-weight:800;
}
</style>
