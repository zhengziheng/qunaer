<!-- 首页推荐组件 -->
<template>
  <div>
    <div class="title" >热销推荐</div>
    <ul>
      <li class="item border-bottom" v-for="item in redommendList" :key="item.id"> 
        <img :src="item.imgUrl" alt="" class="item-img">
        <div class="item-info">
          <p class="item-title">{{item.title}}</p>
          <p class="item-desc">{{item.desc}}</p>
          <button class="item-button">查看详情</button>
        </div>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
name:'HomeRecommend',

  data () {
    return {
      redommendList:[
      {
        id:'0001',
        imgUrl:'http://img1.qunarzz.com/sight/p0/1804/c8/c88bb5e69c9a9c5ea3.img.jpg_200x200_740720ff.jpg',
        title:'北京密云县古北口镇',
        desc:'永顺染，草木色，手工缬，天然彩”。观赏原汁原味的生态印染。老师手把手教你DIY属于自己的印染作品。',
      },
      {
        id:'0002',
        imgUrl:'http://img1.qunarzz.com/sight/p0/1507/36/ce3d2d6c9ab44d67ae68d940b8781829.water.jpg_200x200_0938a8f2.jpg',
        title:'北京野生动物园',
        desc:'北京野生动物园集动物保护、野生动物驯养繁殖及科普教育为一体，汇集了世界各地珍稀野生动物200多种10000余头。',
      },
      {
        id:'0003',
        imgUrl:'http://img1.qunarzz.com/sight/p0/1803/7b/7b023b9728f0834fa3.img.jpg_200x200_5fddc1d8.jpg',
        title:'世界花卉大观园',
        desc:'精品花卉温室展示了各国名优花卉品种和植物造型盆景，其中还增加了一些古船、战车、水车等古老的设施。',
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
.item
  overflow hidden
  display flex
  height 1.9rem
  .item-img
    width 1.7rem
    height 1.7rem
    padding .1rem
  .item-info
    flex 1
    padding .1rem
    min-width 0//可以让flex-item计算出width
    .item-title
      line-height .54rem
      font-size .32rem
    .item-desc
      line-height .4rem
      color #ccc
      ellipsis()
    .item-button
      line-height .44rem
      margin-top .16rem
      background #ff9300
      padding 0 .2rem
      border-radius .06rem
      color #fff
</style>