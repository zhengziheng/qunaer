<!-- 城市列表组件 -->
<template>
    <div>
      <city-header></city-header>
      <city-search></city-search>
    </div>
</template>

<script>
import CityHeader from './components/Header'
import CitySearch from './components/Search'
export default {
name:'City',

  data () {
    return {
    };
  },

props:{},
  components: {
    CityHeader,
    CitySearch,
  },

  computed: {},


  methods: {}
}

</script>
<style lang='stylus' scoped>
</style>