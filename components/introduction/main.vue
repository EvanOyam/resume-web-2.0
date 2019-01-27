<template>
  <div class="introduction-main" :class="{isReady: handleRrady}"></div>
</template>
<script>
export default {
  name: "IntroductionMain",
  data() {
    return {
      handleRrady: false
    };
  },
  components: {},
  mounted() {
    this.handleRrady = true;
  }
};
</script>
<style scoped>
.introduction-main {
  width: 100%;
  height: 100%;
  background-image: url(~assets/pics/content-bg.jpeg);
  background-repeat: no-repeat;
  background-size: 100% 100%;
  transform: translate(0,-100%);
  transition: 0.8s ease-out;
}
.isReady {
  transform: translate(0);
}
</style>

