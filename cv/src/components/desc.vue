<template>
  <div class="desc">
    <div class="time"><span>{{ time }}</span >
      <div  class="line"></div>
  </div>

  <div class="descRight">
      <div><span class="company">{{company}}</span>
    </div>
    <div><span class="position">{{position}}</span>
    </div>
    <div class="experience"><span class="experience-span">{{experience}}</span></div>
  </div>

  </div>
</template>
<script>
  export default {
    props: ["time", "position", "company", "experience"],
    data: function () {
      return {
        title: ''
      }
    },

  }

</script>
<style lang="scss" scoped>
  .line
  {
    background: #3c78d8;
    height: 2px
  }
  .desc {
    flex: 1;
    display: flex;
    justify-content: space-between;
    margin: 20px 0;
  }
  .experience-span
  {
    width: 200px;
    word-wrap:break-word;
  }
  .company {
    margin-left: 5px;
    color: black;
    font-size: 14px;
  }
    span
  
  {
    display: block;
  }
  .position {
    margin-left: 5px;
    color: #92cbb3;
    font-size: 14px;
  }
  
  .time {
    width: 35%
  }
  
  .experience {
    margin-left: 5px;
    color: #a39b9c;
    font-size: 14px;
  }
  
  .descRight {
    width: 65%
  }
 
</style>