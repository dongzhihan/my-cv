<template>
  <div class="desc">
    <h1> {{ time }} </h1>
    <h1>{{company}}</h1>
    <div class="te"></div>
  </div>
</template>

<script>
  export default {
    props: ["time","company"],
    data: function() {
      return {
        title: '' 
      }
    }
    ,
    
  }
</script>

<style   lang="scss" scoped>
 $blue: #3bbfce;
  .desc
  {
    background:$blue
    
  }
        
</style>