<template>
  <div class="skill-main" :class="{isReady: handleRrady}">
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
  name: "SkillMain",
  data() {
    return {
      handleRrady: false,
      content: {
        title: "技能概况",
        detail: [
            `1、硬核心技能：熟练掌握HTML、CSS、JS，熟悉Vue、React等MVVM框架以及周边生态，如Redux，Vuex，Vue-Router以及各类UI库等。
            另外对性能优化，前后端同构方面也有一定了解（事实上本网站就是Vue结合Nuxt首次尝试同构开发），
            同时熟悉jQuery、响应式flex、div+css等传统技术框架或样式布局。`,
            `2、拓展知识：熟悉Node后端，能利用Koa2实现一些后台业务，开发后台系统，同时对Express也有一些了解。
            平时会研究常用算法，网页优化，数据结构等，熟练掌握ajax技术并能使用如axios等优秀的库，能使用如stylus等css预处理，了解webpack等打包工具的知识。`,
            `3、未来目标：进一步加强对前端工程化的了解，更深入啃一啃某一个MVVM框架的源码，以及更深入学习Nuxt。
            此外需要系统化学习webpack，混合开发，性能优化，测试工具，css预处理，CDN等知识。梳理常用数据结构，以及设计模式。然后打算系统学习Go语言。`
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
.skill-main {
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

