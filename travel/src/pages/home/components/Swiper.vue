<template>
  <div class="swiper">
    <swiper :options="swiperOption">
      <swiper-slide v-for="item of swiperData" :key="item.id">
        <img
          class="image"
          :src="item.url"
        >
      </swiper-slide>
      <div class="swiper-pagination" slot="pagination"></div>
    </swiper>
  </div>
</template>

<script>
export default {
  name: "HomeSwiper",
  props: {
    swiperData:Array
  },
  data() {
    return {
      swiperOption: {
        pagination: ".swiper-pagination",
        loop:true
      },
    };
  }
};
</script>

<style lang="stylus" scoped>
  .swiper
    width 100%
    .image
      width 100%

</style>