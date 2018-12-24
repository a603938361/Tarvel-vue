<template>
  <div class="header">
    <div class="header-left">
      <div class="iconfont back-icon">&#xe624;</div>
    </div>
    <div class="header-input">
      <span class="iconfont">&#xe61f;</span>
      输入城市景点/游玩主题
    </div>
    <router-link to="/city">
      <div class="header-right" >
      {{city}}
      <span class="iconfont right-icon">&#xe62d;</span>
    </div>
    </router-link>
  </div>
</template>


<script>
export default {
  name: "HomeHeader",
  props:{
    city:String
  },
};
</script>

<style lang="stylus" scoped>
@import '~styles/varibles.styl';

.header {
  display: flex;
  background-color: $bgColor;
  line-height: $headerHeight
  color: #fff;

  .header-left {
    width: 0.64rem;
    float: left;

    .back-icon {
      text-align: center;
      font-size: 0.3rem;
    }
  }

  .header-input {
    flex: 1;
    background: #fff;
    border-radius: 0.1rem;
    margin-top: 0.12rem;
    line-height: 0.64rem;
    margin-left: 0.2rem;
    color: #ccc;
    height: 0.64rem;
    padding-left: 0.2rem;
  }

  .header-right {
    width: 1.25rem;
    float: right;
    text-align: center;
    color white
    .right-icon {
      font-size: 0.24rem;
    }
  }
}
</style>>

