<!-- 首页组件 -->
<template>
<div>
    <home-header></home-header>
    <home-swiper></home-swiper>
    <home-icons></home-icons>
</div>
</template>

<script>
import HomeHeader from './components/Header'
import HomeSwiper from './components/Swiper'
import HomeIcons from './components/icons'
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
  },

  computed: {},


  methods: {}
}

</script>
<style lang='stylus' scoped>
</style>