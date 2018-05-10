<!-- 详情页组件 -->
<template>
  <div>
    <detail-banner></detail-banner>
    <detail-header></detail-header>
    <div class="content">
      <detail-list :list="list"></detail-list>
    </div>
  </div>
</template>

<script>
import DetailBanner from './components/Banner'
import DetailHeader from './components/Header'
import DetailList from './components/List'
export default {

name:'Detail',

  data () {
    return {
      list:[
        {
          title:'成人票'
        },
        {
          title:'学生票'
        },
        {
          title:'儿童票'
        },
        {
          title:'特惠票'
        },
      ]
    };
  },

props:{},
  components: {
    DetailBanner,
    DetailHeader,
    DetailList,
  },

  computed: {},


  methods: {}
}

</script>
<style lang='stylus' scoped>
.content
  height 50rem
</style>