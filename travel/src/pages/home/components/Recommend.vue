<template>
  <div>
    <div class="title">热销排行</div>
    <ul>
      <li class="item border-bottom" v-for="item of hotListData" :key="item.id">
        <img class="item-img" :src="item.url" alt>

        <div class="item-info">
          <p class="item-title">{{item.title}}</p>
          <p class="item-desc">{{item.desc}}</p>
          <button class="item-button">查看详情</button>
        </div>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: "HomeRecommend",
  props:{
    hotListData:Array
  },
  data() {
    return {
      recommendList: [
        {
          id: "0001",
          url:
            "https://imgs.qunarzz.com/p/tts7/1810/8d/a8bc3d25cee1f402.jpg_180x120_7f3f5dc9.jpg",
          title: "春节特惠！网红海棠湾红树林度假酒店豪华海景房",
          desc: "+接机+自助早+丰富玩乐"
        },
        {
          id: "0002",
          url:
            "https://imgs.qunarzz.com/p/tts0/1810/5b/811d89380e4a702.jpg_180x120_ed218a90.jpg",
          title: "春节预售|超低价来袭！4晚连住三亚湾希尔顿欢朋酒店|赠远洋潜水",
          desc: "+精美旅拍"
        },
        {
          id: "0003",
          url:
            "https://imgs.qunarzz.com/p/tts3/1604/d7/b80c134fb793acf7.jpg_180x120_62ce4f6b.jpg",
          title: "上海直飞厦门纯玩推荐亏本促销 宿市区好评舒适酒店 厦门",
          desc: "+鼓浪屿8大景点"
        }
      ]
    };
  }
};
</script>

<style lang="stylus" scpoed>
@import '~styles/mixins.styl';

.title {
  margin-top: 0.2rem;
  line-height: 0.8rem;
  background: #ccc;
  text-indent: 0.2rem;
}

.item {
  display: flex;
  height: 1.9rem;
  overflow: hidden;

  .item-img {
    width: 1.7rem;
    height: 1.7rem;
    padding: 0.1rem;
  }

  .item-info {
    flex: 1;
    padding: 0.1rem;
    min-width: 0;

    .item-title {
      line-height: 0.54rem;
      font-size: 0.32rem;
      ellipsis();
    }

    .item-desc {
      line-height: 0.4rem;
      color: #ccc;
      ellipsis();
    }

    .item-button {
      margin-top: 0.2rem;
      background: #ff9300;
      padding: 0 0.1rem;
      border-radius: 0.06rem;
    }
  }
}
</style>