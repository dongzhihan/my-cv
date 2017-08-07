<template>
  <div class="point">
    <div><span class="skill">{{skill}}</span></div>
    <div class="ondiv">
      <div class="indiv" v-bind:style="{width:value+'%'}"></div>
    </div>
  </div>
</template>
<script>
  export default {
    props: ["skill", "value"]


  }

</script>
<style lang="scss" scoped>
  .skill {
    color: white
  }

  .ondiv {
    background: black;
    width: 100%;
    height: 20px
  }

  .indiv {
    background: #7cc3a7;
    height: 20px;
  }

</style>
