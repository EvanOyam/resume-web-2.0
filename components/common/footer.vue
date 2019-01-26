<template>
  <div class="footer">
    <el-menu
      :default-active="activeIndex"
      class="el-menu-demo"
      mode="horizontal"
      @select="handleSelect"
      background-color="#395663"
      text-color="#fff"
      active-text-color="#ffd04b"
      router="true"
    >
      <el-row>
        <el-col :span="4">
          <el-menu-item class="el-item" index="/">首页</el-menu-item>
        </el-col>
        <el-col :span="4">
          <el-menu-item class="el-item" index="introduction">自我介绍</el-menu-item>
        </el-col>
        <el-col :span="4">
          <el-menu-item class="el-item" index="skill">技能概况</el-menu-item>
        </el-col>
        <el-col :span="4">
          <el-menu-item class="el-item" index="practice">项目实践</el-menu-item>
        </el-col>
        <el-col :span="4">
          <el-menu-item class="el-item" index="project">实习经历</el-menu-item>
        </el-col>
        <el-col :span="4">
          <el-menu-item class="el-item" index="about">关于本页</el-menu-item>
        </el-col>
      </el-row>
    </el-menu>
  </div>
</template>
<script>
export default {
  name: "HomeFooter",
  data() {
    return {
      activeIndex: "/"
    };
  },
  methods: {
    handleSelect(key, keyPath) {
      console.log(key, keyPath);
    }
  }
};
</script>
<style scoped>
.footer {
  position: absolute;
  bottom: 0;
  right: 0;
  left: 0;
}
.el-item {
  text-align: center;
  border-bottom: 2px solid;
}
</style>

