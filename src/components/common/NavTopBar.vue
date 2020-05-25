<template>
  <div class="nav_top_bar">
    <div class="container">
      <div class="nav_top_bar_left">
        <a href="javascript:;">售后服务</a>
        <a href="javascript:;">帮助中心</a>
        <a href="javascript:;">全年无休热线:400-800-999</a>
      </div>
      <div class="nav_top_bar_right">
        <a href="javascript:;">登录</a>
        <a href="javascript:;">免费注册</a>
        <a href="javascript:;">我的订单</a>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "NavTopBar"
};
</script>

<style lang="scss" scoped>
@import "assets/scss/basic.scss";
@import "assets/scss/config.scss";
@import "assets/scss/mixin.scss";

.nav_top_bar {
  height: 40px;
  background-color: $navcolor;
  .container {
    font-size: $fontJ;
    @include flex(space-between);
    height: 100%;
    .nav_top_bar_left {
      position: relative;
      a {
        margin-left: 10px;
        color: $colorA;
      //兴趣请看mixin,这两个要起用
       @include after();
       @include afterChildBorderNo();
      }
    }

    .nav_top_bar_right {
      position: relative;
      a {
        margin-left: 20px;
        color: $colorA;
        //兴趣请看mixin,这两个要起用
       @include after($ml:5px);
       @include afterChildBorderNo();
      }
    }
  }
}
</style>