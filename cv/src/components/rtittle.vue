<template>
  <div class="tittle">
 
       <div class="tittle-main"><span>{{title}}</span></div>
  </div>
</template>
<script>
  export default {
    props: ["title"]
     

  }

</script>
<style lang="scss" scoped>
 
  .tittle {
    flex:1;
    display: flex;
   
 
 
  }
 
  .tittle-main
  {
      margin-left: 20px;
      color: black;
      font-weight: bolder;
      font-size: 30px
  }
 
</style>
