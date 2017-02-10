<template>
  <div class="tittle">
       <div class="tittle-left"></div>
       <div class="tittle-main"><span>{{title}}</span></div>
  </div>
</template>
<script>
  export default {
    props: ["title"]
     

  }

</script>
<style lang="scss" scoped>
  $blue: #2196f3;
  .tittle {
    flex:1;
    display: flex;
    justify-content: space-between;
 
 
  }
  .tittle-left
  {
      width: 5%;
      background: #4caf50
      
  }
  .tittle-main
  {
      margin-left: 20px;
      color: white;
      font-weight: bolder;
      font-size: 30px
  }
 
</style>
