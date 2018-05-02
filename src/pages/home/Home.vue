<!-- 首页组件 -->
<template>
<div>
    <home-header></home-header>
</div>
</template>

<script>
import HomeHeader from './components/Header'

export default {
    
name:'Home',
  data () {
    return {
    };
  },

  components: {
      HomeHeader,
  },

  computed: {},


  methods: {}
}

</script>
<style lang='stylus' scoped>
</style>