<template>
  <div id="app">  
      <div> <span>{{name}}</span></div>
     <div>
            
            <desco time="2000" company="cx">  </desco>
     </div>
  </div>
</template>

<script>
import desc from './components/desc.vue'
 
export default {
    beforeCreate () {
      console.log(desc)
    },
   data () {
     return {
       name:"董智含"
     }
   },
   
 
        components: {  
            "desco": desc
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
