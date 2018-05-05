<!-- 字母表组件 -->
<template>
  <div class="list">
    <span class="item">A</span>
    <span class="item">A</span>
    <span class="item">A</span>
    <span class="item">A</span>
    <span class="item">A</span>
    <span class="item">A</span>
    <span class="item">A</span>
  </div>
</template>

<script>
export default {
name:'CityAlphabet',

  data () {
    return {
    };
  },

props:{},
  components: {},

  computed: {},


  methods: {}
}

</script>
<style lang='stylus' scoped>
@import '~styles/varibles.styl'
.list 
  display flex
  flex-direction column
  justify-content center
  position absolute
  right 0
  top 1.58rem
  bottom 0
  width .4rem
  // background red
  .item
    text-align center
    line-height .44rem
    color $bgColor
</style>