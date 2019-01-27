<template>
  <div class="project-main" :class="{isReady: handleRrady}">
    <el-row class="row">
      <el-card class="box-card content-box" :body-style="{ height: '100%' }">
        <el-row class="title">{{content.title}}</el-row>
        <el-row class="detail" v-for="(item,index) in content.detail" :key="index">
          <p>{{item}}</p>
        </el-row>
      </el-card>
    </el-row>
  </div>
</template>
<script>
export default {
  name: "ProjectMain",
  data() {
    return {
      handleRrady: false,
      content: {
        title: "项目经历",
        detail: [
          `1、在2018.7月-2018.9月，于广州水滴云有限公司实习，任职前端工程师。
            与团队合作，将公司现有的广州市幼儿园办公系统从PC端移植到微信小程序。
            主要工作： 1、根据需求分析参与原型制作。 2、根据原型编写出小程序页面与实现交互。
             3、提供json请求返回数据规范，配合后端实现接口调用。 4、制作部分自定义控件（组件）。
             5、测试现有demo兼容性问题与debug。`,
          `2、在2018.11月至今，于安正软件-数据管控平台实习，任职前端工程师。主要负责大数据处理类（基金，报表，元数据为主）的门户系统开发
            与数据可视化。主要工作： 1、利用Vue重构各个系统（门户、数据监控与调度、生命资产等）的UI界面与逻辑交互。
             2、负责部分数据可视化工作，将数据以客户需求的方式展示出来。
             3、负责绘图控件追踪，改造并完善元数据绘图、任务监控、调度计划等绘图控件。
             4、维护旧平台。`,
          `3、大学时期曾为“伯雅”设计琴房预约系统，利用Vue与Koa2实现前后端开发。
             自己一步一步填坑，解决诸如300ms点击延迟，1px像素问题，stylus处理css，Koa异步中间件，Vue Router keep alive，利用闭包实现component传参，
             mongoose存储对数组操作等等问题。技术栈为（Vue + Vuex + Vue Router + Stylus + Koa2 + Webpack）。`,
          `4、分别用Vue和React设计个人简历网。（此网站为Vue所建，React版请访问：“http://39.108.112.153:9999”）
             体验用两种不同框架搭建个人简历，目标是快速搭建响应式页面且上线。充分学习components思想，展示组件与容器组件相分离，
             数据状态与单向数据流等知识，解决不同页面中传值问题，对比两种框架开发的不同，ssr同构的异同，以及接触并使用一些优秀的库如react-media，
             等技术栈为（React全家桶 + Vue全家桶 + Nuxt + React Media + Webpack）。`
        ]
      }
    };
  },
  components: {},
  mounted() {
    this.handleRrady = true;
  },
  methods: {}
};
</script>
<style scoped>
.row {
  height: 100%;
  padding: 10% 5%;
  opacity: 0.8;
}
.project-main {
  width: 100%;
  height: 100%;
  background-image: url(~assets/pics/content-bg.jpeg);
  background-repeat: no-repeat;
  background-size: 100% 100%;
  transform: translate(0, -100%);
  transition: 0.8s ease-out;
}
.isReady {
  transform: translate(0);
}
.content-box {
  width: 100%;
  /* background-color: red; */
  margin: 0 auto;
  height: 100%;
  overflow: auto;
}
.title {
  font-size: 2rem;
  font-weight: bold;
  color: #47635b;
  margin-bottom: 40px;
  margin-top: 20px;
}
.detail {
  padding: 20px;
  font-size: 16px;
  text-align: justify;
  font-weight: 700;
  color: #47635b;
  line-height: 40px;
}

.detail p {
  text-indent: 2rem;
}
</style>

