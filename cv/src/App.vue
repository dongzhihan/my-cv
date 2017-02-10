<template>
  <div id="app">
    <div class="name"> <span>{{name}}</span></div>

    <div class="main">
      <div>
        <desco class="desco" time="2000" company="cx" experience="第一次经历"> </desco>
        <desco class="desco" time="2000" company="cx" experience="第一次经历"> </desco>
        <desco class="desco" time="2000" company="cx" experience="第一次经历"> </desco>
      </div>
    </div>
  </div>
</template>
<script>
  import desc from './components/desc.vue'

  export default {
    beforeCreate() {
      console.log(desc)
    },
    data() {
      return {
        name: "董智含"
      }
    },


    components: {
      "desco": desc
    }
  }

</script>
<style scoped>
  #app {

    font-family: 'Avenir', Helvetica, Arial, sans-serif;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    color: #2c3e50;
    margin-top: 60px;
        background: green
  }
  
  .name {
    text-align: center;
    margin-bottom: 50px
  }
  
  .desco {
    width: 200px
  }
  
  .main {
    flex: 1;
    display: flex;
    justify-content: space-between;
    margin: 20px 0;
  }

</style>
