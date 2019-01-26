<template>
  <div class="home-labels">
    <el-row class="first-row row">MY NAME IS</el-row>
    <el-row class="second-row row">
      <div class="name">{{handleName}}</div>
    </el-row>
    <el-row class="third-row row">
      <div class="line"></div>
    </el-row>
    <el-row class="forth-row row">
      <span>{{handleSkill}}</span>
    </el-row>
  </div>
</template>
<script>
export default {
  name: "HomeLabels",
  data() {
    return {
      chineseName: "欧阳智聪",
      englishName: "Evan",
      skill: [
        "JAVASCRIPT",
        "VUE",
        "NODE",
        "KOA",
        "REACT",
        "WEBPACK",
        "HTML",
        "CSS"
      ]
    };
  },
  computed: {
    handleName() {
      return `${this.chineseName}/${this.englishName}`;
    },
    handleSkill() {
      let skill = "";
      let list = this.skill;
      for (let i in list) {
        let item = "";
        if (i == list.length - 1) {
          item = list[i];
        } else {
          item = `${list[i]}/`;
        }
        skill += item;
      }
      return skill;
    }
  }
};
</script>
<style scoped>
.line {
  height: 1px;
  width: 450px;
  background-color: #fff;
  margin: 0 auto;
}
.row {
  color: #fff;
  white-space: nowrap;
  overflow: hidden;
  text-overflow: ellipsis;
  margin: 0 4%;
}
.first-row {
  font-size: 1.6rem;
  margin-top: 50px;
  margin-bottom: 15px;
}
.second-row {
  font-size: 3rem;
  margin-bottom: 20px;
  font-weight: bold;
}
.forth-row {
  font-size: 1rem;
  margin-top: 10px;
  font-weight: bold;
}
</style>

