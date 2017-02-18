<template>
  <div >
      <div class="tittle">
       <div ref="qwe" class="tittle-left"></div>
       <div class="tittle-main"><span>{{title}}</span> 
    </div>
       </div>
       <slot name="children"></slot>
  </div>
</template>
<script>
  export default {
    props: ["title"],
    beforeCreate () {
  
     
    }
     

  }

</script>
<style lang="scss" scoped>
  $blue: #2196f3;
  .tittle {
    flex:1;
    display: flex;
   
 
 
  }
  .tittle-left
  {
      width: 2%;
      background: #7cc3a7
      
  }
 
  .tittle-main
  {
      margin-left: 20px;
      color: white;
      font-weight: bolder;
      font-size: 30px
  }
 
</style>
