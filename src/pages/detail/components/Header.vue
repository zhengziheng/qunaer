<!-- 详情页头部 -->
<template>
  <div>
    <router-link 
    tag="div" 
    to="/" 
    class="header-abs"
    v-show="showAbs"
    >
      <div class="iconfont header-abs-icon">&#xe624;</div>
    </router-link>
    <router-link 
    tag="div" 
    to="/" 
    class="header-fixed"
    v-show="!showAbs"
    :style="opacityStyle"
    >
      <div class="iconfont header-fixed-back">&#xe624;</div>
      景点详情
      </router-link>
  </div>
</template>

<script>
export default {
name:'DetailHeader',

  data () {
    return {
      showAbs:true,
      opacityStyle:{
        opacity:0
      }
    };
  },
activated(){
  window.addEventListener('scroll',this.handleScroll)
},
deactivated(){
  window.removeEventListener('scroll',this.handleScroll)
},
props:{},
  components: {},

  computed: {},


  methods: {
    handleScroll(){
      const top = document.documentElement.scrollTop
      if(top>60){
        let opacity = top/140
        opacity = opacity>1?1:opacity
        this.opacityStyle={
          opacity
        }
        this.showAbs = false
      }else{
        this.showAbs = true
      }
    }
  }
}

</script>
<style lang='stylus' scoped>
@import '~styles/varibles.styl'
.header-abs
  position absolute
  left 0.2rem
  top 0.2rem
  width 0.8rem
  height 0.8rem
  border-radius .4rem
  text-align center
  line-height .8rem
  background rgba(0,0,0,.8)
  .header-abs-icon
    color #ffffff
.header-fixed
  position fixed
  top 0
  left 0
  right 0
  height .86rem
  line-height .86rem
  overflow hidden
  text-align center
  color #fff
  background $bgColor
  font-size .32rem
  z-index 2
  .header-fixed-back
    position absolute
    top 0
    left 0
    width 0.64rem
    text-align center 
    font-size .4rem
    color #fff
</style>