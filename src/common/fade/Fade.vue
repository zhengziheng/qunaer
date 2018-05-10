<!--渐隐动画组件  -->
<template>
  <transition>
  <slot></slot>
  </transition>
</template>

<script>
export default {
name:'Fade',

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
.v-enter,.v-leave-to
  opacity :0
.v-enter-active,.v-leave-active
  transition opacity .5s
</style>