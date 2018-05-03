<!-- 周末游组件 -->
<template>
  <div>
    <div class="title" >周末去哪儿</div>
    <ul>
      <li class="item border-bottom" v-for="item in redommendList" :key="item.id"> 
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
      redommendList:[
      {
        id:'0001',
        imgUrl:'http://img1.qunarzz.com/sight/source/1603/6d/2f67ae0659f41f.jpg_r_640x214_bf6cbd0b.jpg',
        title:'北京赏花好地方',
        desc:'乱花渐欲迷人眼，京城赏花大搜索',
      },
      {
        id:'0002',
        imgUrl:'http://img1.qunarzz.com/sight/source/1505/aa/7baaf8a851d221.jpg_r_640x214_1431200f.jpg',
        title:'北京必游Top10',
        desc:'来北京必去的景点非这些地方莫属',
      },
      {
        id:'0003',
        imgUrl:'http://img1.qunarzz.com/sight/source/1505/9e/21df651e19af5d.jpg_r_640x214_3ea5bb38.jpg',
        title:'世界花卉大观园',
        desc:'数百年的宫廷庙宇，至今依旧威严霸气',
      },
      ]
    };
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
  padding-bottom 33.9%
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