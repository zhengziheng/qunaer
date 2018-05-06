<!-- 字母表组件 -->
<template>
  <div class="list">
    <span class="item" 
    v-for="item in letters" 
    :key="item"
    @click="handleLetterClick"
    @touchstart="handleTouchStart"
    @touchmove="handleTouchMove"
    @touchend="handleTouchEnd"
    :ref="item"
    >{{item}}</span>
  </div>
</template>

<script>
export default {
name:'CityAlphabet',

  data () {
    return {
      touchStatus:false,
      startY:0
    };
  },
updated(){
  this.startY = this.$refs['A'][0].offsetTop
},

props:{
  cities:Object,
},
  components: {},

  computed: {},


  methods: {
    handleLetterClick(e){
      this.$emit('change',e.target.innerText)
      // console.log(e.target.innerText);
      
    },
    handleTouchStart(){
      this.touchStatus = true
    },
    handleTouchMove(e){
      if(this.touchStatus===true){
        const touchY = e.touches[0].clientY-79
        const index = Math.floor((touchY-this.startY)/20)
        if(index >= 0&& index < this.letters.length){
          this.$emit('change',this.letters[index])

        }
      }
    },
    handleTouchEnd(){
      this.touchStatus = false
    }

  },
  computed:{
    letters(){
      const letters = []
      for (let i in this.cities){
        letters.push(i)
      }
      return letters
    }
  }
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