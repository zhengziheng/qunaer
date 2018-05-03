<!-- 首页组件 -->
<template>
<div>
    <home-header></home-header>
    <home-swiper></home-swiper>
    <home-icons></home-icons>
    <home-recommend></home-recommend>
</div>
</template>

<script>
import HomeHeader from './components/Header'
import HomeSwiper from './components/Swiper'
import HomeIcons from './components/icons'
import HomeRecommend from './components/recommend'
export default {
    
name:'Home',
  data () {
    return {
    };
  },

  components: {
      HomeHeader,
      HomeSwiper,
      HomeIcons,
      HomeRecommend,
  },

  computed: {},


  methods: {}
}

</script>
<style lang='stylus' scoped>
</style>