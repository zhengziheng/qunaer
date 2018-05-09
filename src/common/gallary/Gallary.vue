<!-- 画廊组件 -->
<template>
  <div class="container" @click="handleGallaryClick">
    <div class="wrapper">
      <swiper :options="swiperOptions">
        <swiper-slide v-for="(item,index) in imgs" :key="index">
          <img  class="gallary-img" :src="item" alt="">
        </swiper-slide>
        <div class="swiper-pagination"  slot="pagination"></div>
      </swiper>
    </div>
  </div>
</template>

<script>
export default {
name:'CommonGallary',

  data () {
    return {
      swiperOptions:{ 
        pagination : '.swiper-pagination',
        paginationType : 'fraction',
        observeParents:true, //检测dom元素或者父级dom元素发生变化自动刷新一次
        observer:true

      }
    };
  },

props:{
  imgs:{
    type:Array,
    default(){
      return []
    }
  }
},
  components: {},

  computed: {},


  methods: {
    handleGallaryClick(){
      this.$emit('close')

    }
  }
}

</script>
<style lang='stylus' scoped>
.container >>>.swiper-container
  overflow inherit 
.container
  display  flex
  position fixed
  flex-direction column
  justify-content center
  z-index 99
  left 0
  right 0
  top 0
  bottom 0
  background #000
  .wrapper
    width 100%
    height 0
    padding-bottom 100%
    // overflow hidden
    .gallary-img
      width 100%
    .swiper-pagination
      color #fff
      bottom -1rem
</style>