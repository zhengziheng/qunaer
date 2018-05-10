<!-- 详情页组件 -->
<template>
  <div>
    <detail-banner></detail-banner>
    <detail-header></detail-header>
    <div class="content"></div>
  </div>
</template>

<script>
import DetailBanner from './components/Banner'
import DetailHeader from './components/Header'
export default {

name:'Detail',

  data () {
    return {
    };
  },

props:{},
  components: {
    DetailBanner,
    DetailHeader,
  },

  computed: {},


  methods: {}
}

</script>
<style lang='stylus' scoped>
.content
  height 50rem
</style>