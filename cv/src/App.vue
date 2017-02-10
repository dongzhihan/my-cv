<template>
  <div id="app">
    <div class="name"> <span>{{name}}</span></div>
    <div class="main">
       
        <div class="main-left">
          <div class="hello"><span>hello</span></div>
          <d-tittle title="abount me"></d-tittle>
          <desco class="desco" v-for="(item,index) in experiences" v-bind:time="item.time" v-bind:company="item.company" v-bind:experience="item.experience">
          </desco>
        </div>
        <div class="main-right"> </div>
 
    </div>
</template>
<script>
  import desc from './components/desc.vue'
   import tittle from './components/tittle.vue'
  export default {
    beforeCreate() {
      console.log(desc)
    },
    data() {
      return {
        name: "董智含",
        experiences: [{
            time: 2000,
            company: "cx",
            experience: "第一次"
          },
          {
            time: 2000,
            company: "cx",
            experience: "第二次"
          }

        ]
      }
    },


    components: {
      "desco": desc,
      "d-tittle":tittle
    }
  }

</script>
<style scoped>
  #app {
    font-family: 'Avenir', Helvetica, Arial, sans-serif;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    color: #2c3e50;
    background: #009688;
    width: 800px;
    margin: 0 auto;
  }
  
  .name {
    text-align: center;
    margin-bottom: 50px
  }
  
  .desco {
  
  }
  
  .main {
    flex: 1;
    display: flex;
    justify-content: space-between;
    width: 100%;
    margin: 20px 0;
  }
  
  .main-left {
    width: 40%
  }
  
  .main-right {
    width: 60%
  }
  
  .hello {
    text-align: center;
    font-size: 60px;
    font-weight: bolder;
    color: white;
    margin-bottom: 100px
  }

</style>
