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
      :router="true"
    >
      <el-row>
        <el-col :span="6" v-for="(item,index) in list" :key="index">
          <el-menu-item class="el-item" :index="item.index">{{item.title}}</el-menu-item>
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
      activeIndex: "/",
      list: [
        {
          index: "/",
          title: "首页"
        },
        {
          index: "/introduction",
          title: "简介"
        },
        {
          index: "/skill",
          title: "技能"
        },
        {
          index: "/project",
          title: "项目"
        },
      ]
    };
  },
  mounted() {
    this.activeIndex = this.$route.path;
  },
  methods: {
    handleSelect(key, keyPath) {
      console.log(key);
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

