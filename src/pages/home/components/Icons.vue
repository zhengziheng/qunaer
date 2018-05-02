<!--首页图标导航组件  -->
<template>
  <div class="icons">
    <div class="icon">
      <div class="icon-img">
      <img class="icon-img-content" src="http://img1.qunarzz.com/piao/fusion/1803/95/f3dd6c383aeb3b02.png" alt="">
      </div>
      <p class="icon-desc">景点门票</p>
    </div>
    <div class="icon">
      <div class="icon-img">
      <img class="icon-img-content" src="http://img1.qunarzz.com/piao/fusion/1804/ff/fdf170ee89594b02.png" alt="">
      </div>
      <p class="icon-desc">必游榜单</p>
    </div>
    <div class="icon">
      <div class="icon-img">
      <img class="icon-img-content" src="http://img1.qunarzz.com/piao/fusion/1803/bd/9f7b9b2b60c1502.png" alt="">
      </div>
      <p class="icon-desc">踏青赏花</p>
    </div>
    <div class="icon">
      <div class="icon-img">
      <img class="icon-img-content" src="http://img1.qunarzz.com/piao/fusion/1804/5a/13ceb38dcf262f02.png" alt="">
      </div>
      <p class="icon-desc">一日游</p>
    </div>
    <div class="icon">
      <div class="icon-img">
      <img class="icon-img-content" src="http://img1.qunarzz.com/piao/fusion/1803/76/eb88861d78fb9902.png" alt="">
      </div>
      <p class="icon-desc">动植物园</p>
    </div>
    <div class="icon">
      <div class="icon-img">
      <img class="icon-img-content" src="http://img1.qunarzz.com/piao/fusion/1803/6c/9e54a8540fee0102.png" alt="">
      </div>
      <p class="icon-desc">故宫</p>
    </div>
    <div class="icon">
      <div class="icon-img">
      <img class="icon-img-content" src="http://img1.qunarzz.com/piao/fusion/1803/67/9a1678221b8e0e02.png" alt="">
      </div>
      <p class="icon-desc">古北水镇</p>
    </div>
    <div class="icon">
      <div class="icon-img">
      <img class="icon-img-content" src="http://img1.qunarzz.com/piao/fusion/1804/ed/cf572be30fc32f02.png" alt="">
      </div>
      <p class="icon-desc">Q+精选</p>
    </div>
    
      icons
  </div>
</template>

<script>
export default {
name:'HomeIcons',

  data () {
    return {
    };
  },

  components: {},

  computed: {},


  methods: {}
}

</script>
<style lang='stylus' scoped>
@import '~styles/varibles.styl'
.icons
  width 100%
  overflow hidden
  height 0
  padding-bottom 50%//宽度设置为100%，高站位为宽的50%
  .icon
    position relative
    overflow hidden
    float left
    height 0
    width 25%
    padding-bottom 25%//width 25% paddingbottom 25% 设置图标的宽高为父容器的 25%
    .icon-img
      position absolute
      top 0
      left 0
      right 0
      bottom .44rem
      box-sizing border-box
      padding .1rem
      .icon-img-content
        display block
        margin 0 auto
        height 100%
    .icon-desc
      position absolute
      left 0
      right 0
      bottom 0
      height .44rem
      line-height .44rem
      color $darkTextColor
      text-align center 
</style>