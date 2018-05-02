<!-- 首页的轮播图组件 -->
<template>
<div class="wrapper">
  <swiper :options="swiperOption" >
    <swiper-slide v-for="item in swiperList" :key="item.id">
        <img  class="swiper-img" :src="item.imgUrl" alt="">
    </swiper-slide>

    <div class="swiper-pagination"  slot="pagination"></div>
  </swiper>
</div>
</template>

<script>
export default {
name:'HomeSwiper',
  data () {
    return {
        swiperOption: {
          pagination:'.swiper-pagination',
          loop:true,
        },
        swiperList:[{
          id:'0001',
          imgUrl:'http://img1.qunarzz.com/piao/fusion/1804/fa/1932440360b42e02.jpg_640x200_07b74613.jpg'
        },
        {
          id:'0002',
          imgUrl:'http://img1.qunarzz.com/piao/fusion/1803/eb/f3d2fa5308fd5f02.jpg_640x200_4f36f53a.jpg'
        },
        {
          id:'0003',
          imgUrl:'http://img1.qunarzz.com/piao/fusion/1804/f7/a1306242ecc0202.jpg_640x200_294049d2.jpg'
        }
        ]
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