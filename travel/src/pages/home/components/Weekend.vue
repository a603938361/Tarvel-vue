<template>
  <div>
    <div class="title">周末两日游</div>
    <ul>
      <li class="witem border-bottom" v-for="item of weekendList" :key="item.id">
        <div class="witem-img-wrapper">
          <img class="witem-img" :src="item.url" alt>
        </div>
        <div class="witem-info">
          <p class="witem-title">{{item.title}}</p>
          <p class="witem-desc">{{item.desc}}</p>
        </div>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: "HomeWeekend",
  props:{
    weekendList:Array
  },
};
</script>

<style lang="stylus" scpoed>
@import '~styles/mixins.styl';

.title {
  margin-top: 0.2rem;
  line-height: 0.8rem;
  background: #ccc;

  text-indent 0.2rem {
    .witem-img-wrapper {
      overflow: hidden;
      height: 0;
      padding-bottom: 37.09%;

      .witem-img {
        width: 100%;
      }
    }

    .witem-info {
      padding: 0.1rem;
      background: red;

      .witem-title {
        line-height: 0.54rem;
        font-size: 0.32rem;
        ellipsis();
      }

      .witem-desc {
        line-height: 0.4rem;
        color: #cccccc;
        ellipsis();
      }
    }
  }
}
</style>