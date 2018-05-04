<!-- 首页的轮播图组件 -->
<template>
<div class="wrapper">
  <swiper :options="swiperOption" v-if="list.length">
    <swiper-slide v-for="item in list" :key="item.id">
        <img  class="swiper-img" :src="item.imgUrl" alt="">
    </swiper-slide>

    <div class="swiper-pagination"  slot="pagination"></div>
  </swiper>
</div>
</template>

<script>
export default {
name:'HomeSwiper',
props:{
list:{
  type:Array, 
}
},
  data () {
    return {
        swiperOption: {
          pagination:'.swiper-pagination',
          loop:true,
        },
    };
  },

  components: {},

  computed: {},


  methods: {}
}

</script>
<style lang='stylus' scoped>
//>>>表示样式穿透，wrapper里面的class都可以用（忽略scoped），不管他是否属于别的组件
.wrapper >>> .swiper-pagination-bullet-active
    background #fff
.wrapper
  width 100%
  height 0
  overflow hidden
  padding-bottom 31.25%
  .swiper-pagination-bullet-active
    background red
  .swiper-img
    width 100%
</style>