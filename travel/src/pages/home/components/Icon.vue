<template>
  <div class="icons">
    <div class="icon" v-for="item of iconData" :key="item.id">
      <img class="img" :src="item.url">
      <p class="text">{{item.desc}}</p>
    </div>
  </div>
</template>

<script>
export default {
  name: "Icon",
  props:{
      iconData:Array
  },
};
</script>

<style lang="stylus" scoped>
.icons {
  width: 100%;
  height: 0;
  padding-bottom: 50%;
  margin-top 10px

  .icon {
    float: left;
    width: 25%;
    height: 25%;
    padding-bottom: 25%;

    .img {
      width: 70px;
      height: 70px;
      margin-left: 12px;
    }

    .text {
      font-size: 12px;
      line-height: 22px;
      text-align: center;
      margin-bottom: 10px;
    }
  }
}
</style>