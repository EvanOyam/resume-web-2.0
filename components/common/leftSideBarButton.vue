<template>
  <div class="button-box">
    <el-row class="button-group" :gutter="10">
      <el-col :span="6" class="col" v-for="(item, index) in icons" :key="index">
        <div class="icon" :class="item.name" @click="open(item)"></div>
      </el-col>
    </el-row>
  </div>
</template>
<script>
export default {
  name: "Button",
  components: {},
  data() {
    return {
      icons: [
        {
          name: "phone",
          label: "我的电话是：",
          information: "17612020299"
        },
        {
          name: "email",
          label: "我的邮箱是：",
          information: "953328679@qq.com"
        },
        {
          name: "wechat",
          label: "我的微信是：",
          information: "13827232129"
        },
        {
          name: "github",
          label: "我的github是：",
          information: "https://github.com/EvanOyam"
        }
      ]
    };
  },
  methods: {
    open(item) {
      this.$alert(`${item.information}`, `${item.label}`, {
        confirmButtonText: "确定",
        callback: action => {
          this.$message({
            type: "success",
            message: `记得联系我哦！`
          });
        }
      });
    }
  }
};
</script>
<style scoped>
.button-box {
  transition: width 1s ease-out;
  width: 90%;
  margin: 0 auto;
}
.phone {
  background-image: url(~assets/pics/phone.png);
}
.wechat {
  background-image: url(~assets/pics/wechat.png);
}
.github {
  background-image: url(~assets/pics/github.png);
}
.email {
  background-image: url(~assets/pics/email.png);
}
.icon {
  transition: 1s;
  width: 40px;
  height: 40px;
  border: 2px solid #fff;
  border-radius: 100px;
  margin: 0 auto;
  background-position: 50% 50%;
  background-size: 24px;
  background-repeat: no-repeat;
}
.icon:hover {
  border: 2px solid #ffd04b;
  transform: scale(1.2);
  cursor: pointer;
}
</style>
