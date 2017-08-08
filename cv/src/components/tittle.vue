<template>
  <div >
      <div class="tittle">
       <div   class="tittle-left"></div>
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

     margin: 24px 0;

  }
  .tittle-left
  {
      width: 2%;
      background: #7cc3a7

  }

  .tittle-main
  {
      margin-left: 40px;
      color: white;
      font-weight: bolder;
      font-size: 30px
  }

</style>
