<template>
  <div>
      <HomeHeader :city="city"></HomeHeader>
      <HomeSwiper :swiperData = "swiperData"></HomeSwiper>
      <icon :iconData="iconData"></icon>
      <HomeRecemmend :hotListData="hotListData"></HomeRecemmend>
      <HomeWeekend :weekendList="weekendList"></HomeWeekend>
  </div>
</template>


<script>
import HomeHeader from './components/Header'
import HomeSwiper from './components/Swiper'
import Icon from './components/Icon'
import HomeRecemmend from './components/Recommend'
import HomeWeekend from './components/Weekend'

import axios from 'axios'

export default {
  name: "Home",
  components:{
      HomeHeader,
      HomeSwiper,
      Icon,
      HomeRecemmend,
      HomeWeekend
  },
  
  data() {
    return {
      city:'',
      swiperData:[],
      iconData:[],
      hotListData:[],
      weekendList:[]
    }
  },

  mounted(){
    axios.get('/static/mock/index.json')
    .then(res=>{
      console.log('res: ', res);
      this.city = res.data.city
      this.swiperData = res.data.data.swiperList
      this.iconData = res.data.data.iconList
      this.hotListData = res.data.data.recommendList
      this.weekendList = res.data.data.weekendList
    }).catch(error=>{
      console.log('error: ', error);
    })
  }
};
</script>

<style>
</style>
