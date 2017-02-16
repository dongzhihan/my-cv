<template>
  <div id="app">
    <div class="main">
      <div class="main-left">
        <div class="hello"><span>hello</span></div>
        <d-tittle title="abount me">
          <div class="name" slot="children"> <span>{{name}}</span></div>
        </d-tittle>
        <d-tittle title="skills">
          <div class="skills" slot="children">
            <point v-for="(item,index) in skills" v-bind:skill="item.skill" v-bind:value="item.value"></point>
          </div>
        </d-tittle>
        <d-tittle title="message">
          <div class="message-div" slot="children">
            <p><b>地址：</b>苏州市工业园区</p>
            <p><b>电话：</b>18626161645</p>
            <p><b>Email：</b>529211933@qq.com</p>
            <p><b>github：</b><a href="https://dongzhihan.github.com/">https://dongzhihan.github.com/</a></p>
          </div>
        </d-tittle>
      </div>




      <div class="main-right">
        <div class="cv"><span>{{mycv}}</span></div>
        <r-tittle title="experience"></r-tittle>
        <div>
          <desco class="desco" v-for="(item,index) in experiences" v-bind:position="item.position" v-bind:time="item.time" v-bind:company="item.company"
            v-bind:experience="item.experience">
            </desco>
        </div>
      </div>
    </div>
</template>
<script>
  import desc from './components/desc.vue'
  import tittle from './components/tittle.vue'
  import rtittle from './components/rtittle.vue'
  import point from './components/point.vue'
  export default {
    beforeCreate() {

    },
    data() {
      return {
        mycv: "我的cv",
        name: "xxxxxxxxxxxxxxxxxxxxx",
        experiences: [{
          time: "2000-1-2~2000-1-3",
          company: "cx",
          experience: "第一次11111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111",
          position: "1"
        },
        {
           time: "2000-1-2~2000-1-3",
          company: "cx",
          experience: "第二次1112222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222",
          position: "2"
        }
,
        {
           time: "2000-1-2~2000-1-3",
          company: "cx",
          experience: "第三次1112222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222222",
          position: "3"
        }
        ],
        skills: [
          {
            skill: "1",
            value: 80

          },
          {
            skill: "2",
            value: 50

          }, {
            skill: "3",
            value: 75

          }

        ]
      }
    },


    components: {
      "desco": desc,
      "d-tittle": tittle,
      "r-tittle": rtittle,
      "point": point
    }
  }

</script>
<style scoped>
  #app {
    font-family: 'Avenir', Helvetica, Arial, sans-serif;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    color: #2c3e50;
    width: 800px;
    margin: 0 auto;
  }
  
  .point {
    width: 100%;
    height: 50px
  }


  .cv {
    font-size: 30px;
    color: black;
    text-align: center;
    font-weight: bolder;
    margin-bottom: 50px;
  }
  
  .name {
    margin-bottom: 50px;
    width: 100%;
    margin-left: 24px;
    color: white
  }
  
  .message-div {
    margin-left: 24px;
    color: white
  }
  
  .skills {
    margin-left: 24px;
  }
  
  .desco {}
  
  .main {
    flex: 1;
    display: flex;
    justify-content: space-between;
    width: 100%;
    margin: 20px 0;
  }
  
  .main-left {
    width: 40%;
    background: #2a3a4a
  }
  
  .main-right {
    width: 60%
  }
  
  .hello {
    text-align: center;
    font-size: 60px;
    font-weight: bolder;
    color: white;
    margin-bottom: 100px;
    margin-left: 20px;
  }
</style>