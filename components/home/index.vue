<template>
  <div>
    <el-container>
      <el-main>
        <home-body></home-body>
      </el-main>
      <home-footer></home-footer>
    </el-container>
  </div>
</template>
<script>
import homeBody from "./body";
import homeFooter from "../common/footer";
export default {
  name: "Home",
  components: {
    homeBody,
    homeFooter
  }
};
</script>
<style scoped>
.el-footer {
  background-color: #b3c0d1;
  color: #333;
  text-align: center;
  height: 8% !important;
}
.el-main {
  background-color: #e9eef3;
  color: #333;
  text-align: center;
  height: 94%;
  position: relative;
}
.el-container {
  position: absolute;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
}
</style>

