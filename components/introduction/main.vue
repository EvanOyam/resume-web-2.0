<template>
  <div class="introduction-main" :class="{isReady: handleRrady}">
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
  name: "IntroductionMain",
  data() {
    return {
      handleRrady: false,
      content: {
        title: "自我介绍",
        detail: [
          `大家好，我叫欧阳智聪，1997年出生，广东东莞人，就读于广东财经大学信息学院，信息管理与信息系统专业（IMIS），
          于2015年入学，是19年应届毕业生。在校内主修计算机领域方面的知识，学习包括数据结构，计算机组成原理，C语言，
          数据库原理，系统设计等多门计算机学科。`,
          `在大学期间曾联合创立“伯雅音乐”高校音乐传媒，连续两届校创业竞标冠军，省百项工程重点项目。
          热爱编程，设计学生管理系统，琴房预约系统，后用Vue与Koa2重构。自大一起开始对前端领域感兴趣，大二开始接触包括UI框架，数据分离思路，
          性能优化，异步请求等多种知识体系`,
          `热爱生活，喜欢旅行，摄影，也曾担任乐队吉他手，自己写过歌，穿越草原无人区拍摄银河。
          喜欢研究各种Web技术，关注大牛动态，研究并学习MVVM框架，Web性能优化，前后端同构SEO优化，前端工程化等，希望未来自己能不断进步！`
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
.introduction-main {
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

