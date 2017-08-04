<template>
  <div id="app">
    <div class="app-main">
      <div class="top-main">
        <div class="top">前端开发</div>
        <div class="top-bottm">
          <div class="top-bottm-center">
            <div class="im"><span>I'm</span></div>
            <div class="top-bottm-center"><span style="font-size: 24px; font-weight: 700; letter-spacing: 5px;">董智含</span><br><span>前端工程师</span></div>
          </div>
        </div>
      </div>
      <div class="main">

        <div class="main-left">

          <d-tittle title="abount me">
            <div class="name" slot="children"> <span>{{name}}</span></div>
          </d-tittle>
          <d-tittle title="skills">
            <div class="skills" slot="children">
              <point class="skill" v-for="(item,index) in skills" v-bind:skill="item.skill" v-bind:value="item.value"></point>
            </div>
          </d-tittle>
          <d-tittle title="message">
            <div class="message-div" slot="children">
              <p><b>地址：</b>苏州市工业园区</p>
              <p><b>电话：</b>18626161645</p>
              <p><b>Email：</b>529211933@qq.com</p>
              <p><b>github：</b><a href="https://github.com/dongzhihan">https://github.com/dongzhihan</a></p>
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
    </div>
  </div>
</template>
<script>
  import desc from './components/desc.vue'
  import tittle from './components/tittle.vue'
  import rtittle from './components/rtittle.vue'
  import point from './components/point.vue'
  export default {

    data() {
      return {
        mycv: "",
        name: "2年前端开发经验，参与过多次大型网站的开发，涉及仓库、电商、工厂等方面。 熟悉es6、es7，用过angular、vue等框架，开发过hrbird app，熟练使用git等版本控制工具 为人谦虚谨慎，实事求是，对新技术抱有强烈好奇心。",
        experiences: [{
            time: "2016-7~至今",
            company: "精易会",
            experience: "负责使用angular和vue对pda、pc端页面编写",
            position: "前端工程师"
          },
          {
            time: "2017-2~至今",
            company: "业余",
            experience: "使用vue编写了一个云笔记系统",
            position: "前端工程师"
          }
        ],
        skills: [{
            skill: "node.js",
            value: 70
          },
          {
            skill: "vue",
            value: 80

          }, {
            skill: "angular",
            value: 75
          }, {
            skill: "jquery",
            value: 80
          }, {
            skill: "es6/7",
            value: 80
          }, {
            skill: "git/SVN",
            value: 80
          }, {
            skill: "CSS/CSS3",
            value: 80
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
    color: #2c3e50;
  }

  .app-main {
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
    margin-left: 24px;
    color: white;
    padding: 10px 30px 20px 30px;
    font-size: 14px;
  }

  .message-div {
    margin-left: 24px;
    color: white
  }

  .skills {
        padding: 10px 30px 20px 30px;
  }

  .desco {}

  .main {
    flex: 1;
    display: flex;
    justify-content: space-between;
    width: 100%;
    margin: 1px 0;
  }

  .main-left {
    width: 45%;
    background: #2a3a4a
  }

  .main-right {
    width: 55%
  }

  .hello {
    text-align: center;
    font-size: 60px;
    font-weight: bolder;
    color: white;
    margin-bottom: 100px;
    margin-left: 20px;
  }

  .top-main {
    display: -webkit-box;
    display: -moz-box;
    display: -ms-flexbox;
    display: -webkit-flex;
    display: flex;
    justify-content: space-between;
    align-items: center;
    background: #7cc3a7;
    color: #fff;
    padding: 36px 0;
  }

  .top {
    flex: 4;
    display: -webkit-box;
    display: -moz-box;
    display: -ms-flexbox;
    display: -webkit-flex;
    display: flex;

    justify-content: center;
    align-items: center;
    font-size: 36px;
  }

  .top-bottm {
    flex: 6;
    display: -webkit-box;
    display: -moz-box;
    display: -ms-flexbox;
    display: -webkit-flex;
    display: flex;
    justify-content: center;
    align-items: center;
  }

  .im:after {
    content: '';
    position: absolute;
    left: 0;
    right: 0;
    margin: auto;
    top: 100%;
    margin: auto;
    width: 0;
    height: 0;
    border: 7px solid;
    border-color: #374046 rgba(0, 0, 0, 0) rgba(0, 0, 0, 0) rgba(0, 0, 0, 0);
  }

  .im {
    display: inline-block;
    padding: 3px 8px;
    background: #374046;
    border-radius: 5px;
    text-align: center;
    position: relative;
    margin-bottom: 5px;
  }

  .skill {
    margin-bottom: 10px;
  }

</style>
