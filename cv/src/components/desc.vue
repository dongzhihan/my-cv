<template>
  <div class="desc">
    <div class="time"><span>{{ time }}</span ><div><span class="company">{{company}}</span></div></div>
    <div class="experience"><span class="experience-span">{{experience}}</span></div>
  </div>
</template>
<script>
  export default {
    props: ["time", "company","experience"],
    data: function () {
      return {
        title: ''
      }
    },

  }

</script>
<style lang="scss" scoped>
  $blue: #3bbfce;
  .desc {
    flex:1;
    display: flex;
    justify-content: space-between;
    margin: 20px 0;
    background: $blue
  }
  
  .company {
    margin-left: 5px
  }
  
 .time
 {
   width: 30%
 }
 .experience
 {
   width: 60%
 }

</style>
