<template>
  <div class="left-side-bar-box" :style="bgColor" :class="{isReady: handleRrady}">
    <el-row class="row">
      <protrait class="left-side-bar-protrait"></protrait>
    </el-row>
    <el-row class="row information-row">
      <el-table :data="tableData" style="width: 100%" class="table" :style="tableBgColor">
        <el-table-column prop="label" label="姓名"></el-table-column>
        <el-table-column prop="detail" label="欧阳智聪"></el-table-column>
      </el-table>
    </el-row>
    <el-row class="row button-row">
      <left-side-button></left-side-button>
    </el-row>
  </div>
</template>
<script>
import protrait from "./portrait";
import leftSideButton from "./leftSideBarButton";
export default {
  name: "LeftSideBar",
  components: {
    leftSideButton,
    protrait
  },
  data() {
    return {
      tableBgColor: {
        backgroundColor: ""
      },
      bgColor: {
        backgroundColor: ""
      },
      handleRrady: false,
      tableData: [
        {
          label: "性别：",
          detail: "男"
        },
        {
          label: "年龄：",
          detail: "21岁"
        },
        {
          label: "毕业院校（应届毕业）：",
          detail: "广东财经大学"
        },
        {
          label: "应聘岗位：",
          detail: "前端开发工程师"
        }
      ]
    };
  },
  mounted() {
    let path = this.$route.path;
    switch (path) {
      case "/introduction":
        this.bgColor.backgroundColor = "#63757E";
        this.tableBgColor.backgroundColor = "#63757E";
        break;
      case "/skill":
        this.bgColor.backgroundColor = "#6F3448";
        this.tableBgColor.backgroundColor = "#6F3448";
        break;
      case "/project":
        this.bgColor.backgroundColor = "#BC5654";
        this.tableBgColor.backgroundColor = "#BC5654";
        break;
      default:
        break;
    }
    this.handleRrady = true;
  },
  methods: {}
};
</script>
<style scoped>
.left-side-bar-box {
  width: 100%;
  height: 100%;
  transform: translate(-100%);
  transition: 0.8s ease-out;
}
.isReady {
  transform: translate(0);
}
.left-side-bar-protrait {
  margin-top: 100px;
}
.row {
  width: 90%;
  margin: 0 auto;
}
.table {
  color: #fff;
  width: 100%;
  margin: 0 auto;
}
.information-row {
  margin-top: 100px;
}
.button-row {
  margin-top: 50px;
}
</style>

<style>
.el-table__body tr:hover > td {
  transition: .5s;
  background: #919191 !important;
  color: #ffd04b !important;
}
</style>


