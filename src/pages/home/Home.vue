<!-- 首页组件 -->
<template>
<div>
    <home-header ></home-header>
    <home-swiper :list="swiperList"></home-swiper>
    <home-icons :iconList="iconList"></home-icons>
    <home-recommend :recommendList="recommendList"></home-recommend>
    <home-weekend :weekendList="weekendList"></home-weekend>
</div>
</template>

<script>
import HomeHeader from './components/Header'
import HomeSwiper from './components/Swiper'
import HomeIcons from './components/Icons'
import HomeRecommend from './components/Recommend'
import HomeWeekend from './components/Weekend'
import axios from 'axios'
import {mapState} from 'vuex'
export default {
    
name:'Home',
  data () {
    return {
      lastCity:'',
      swiperList:[],
      iconList:[],
      recommendList:[],
      weekendList:[]
    };
  },

  components: {
      HomeHeader,
      HomeSwiper,
      HomeIcons,
      HomeRecommend,
      HomeWeekend,
  },

  mounted(){
    this.getHomeInfo()
    this.lastCity = this.city

    
  },

  computed: {
    ...mapState(['city'])
  },


  methods: {
    getHomeInfo(){
      axios.get('/api/index.json?city= +this.city')
      .then(this.getHomeInfoSucc)
    },
    getHomeInfoSucc(res){
      res = res.data
      if(res.ret&&res.data){
        const data = res.data
        this.swiperList = data.swiperList
        this.iconList = data.iconList
        this.recommendList = data.recommendList
        this.weekendList = data.weekendList
      }
      
    }
  },
  activated(){
    //页面被缓存的时候，修改缓存页面用这个生命周期钩子
    if(this.lastCity!==this.city){
      this.lastCity = this.city
      this.getHomeInfo()
    }
  }
}

</script>
<style lang='stylus' scoped>
</style>