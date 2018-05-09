<!-- 详情页组件 -->
<template>
  <div>
    <detail-banner></detail-banner>
  </div>
</template>

<script>
import DetailBanner from './components/Banner'
export default {

name:'Detail',

  data () {
    return {
    };
  },

props:{},
  components: {
    DetailBanner,
  },

  computed: {},


  methods: {}
}

</script>
<style lang='stylus' scoped>
</style>