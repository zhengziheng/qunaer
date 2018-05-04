<!-- 周末游组件 -->
<template>
  <div>
    <div class="title" >周末去哪儿</div>
    <ul>
      <li class="item border-bottom" v-for="item in weekendList" :key="item.id"> 
        <div class="item-img-wrapper">
        <img :src="item.imgUrl" alt="" class="item-img">
        </div>
        <div class="item-info">
          <p class="item-title">{{item.title}}</p>
          <p class="item-desc">{{item.desc}}</p>
          <!-- <button class="item-button">查看详情</button> -->
        </div>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
name:'HomeWeekend',

  data () {
    return {
    };
  },
  props:{
    weekendList:{
      type:Array
    }
  },

  components: {},

  computed: {},


  methods: {}
}

</script>
<style lang='stylus' scoped>
@import '~styles/mixins.styl'
.title
  margin-top .2rem
  line-height .8rem
  background #eee
  text-indent .2rem
.item-img-wraper
  overflow hidden
  height 0
  padding-bottom 37.09%
.item-img
  width 100%
.item-info
  flex 1
  padding .1rem
  min-width 0//可以让flex-item计算出width
  .item-title
    line-height .54rem
    font-size .32rem
  .item-desc
    line-height .4rem
    ellipsis()
 
</style>