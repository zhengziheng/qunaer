<!-- 城市列表组件 -->
<template>
    <city-header></city-header>
</template>

<script>
import CityHeader from './components/Header'
export default {
name:'City',

  data () {
    return {
    };
  },

props:{},
  components: {
    CityHeader,
  },

  computed: {},


  methods: {}
}

</script>
<style lang='stylus' scoped>
</style>