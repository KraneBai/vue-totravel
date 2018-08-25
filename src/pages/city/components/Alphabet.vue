<template>
  <ul class="alphabet">
    <li class="item"
      v-for="item of letters"
      :key="item"
      :ref="item"
      @click="getLetter"
      @touchstart="touchStart"
      @touchmove="touchMove"
      @touchend="touchEnd"
    >{{item}}</li>
  </ul>
</template>
<script>
export default {
  name: 'CityAlphabet',
  props: {
    cities: Object
  },
  data () {
    return {
      touchStatus: false,
      startY: 0,
      timer: null
    }
  },
  // 页面完成了自己的渲染
  updated () {
    this.startY = this.$refs['A'][0].offsetTop
  },
  computed: {
    letters () {
      const letters = []
      for (var item in this.cities) {
        letters.push(item)
      }
      return letters
    }
  },
  methods: {
    getLetter (e) {
      this.$emit('change', e.target.innerText)
    },
    touchStart () {
      this.touchStatus = true
    },
    touchEnd () {
      this.touchStatus = false
    },
    touchMove (e) {
      if (this.touchStatus) {
        if (this.timer) {
          // touchmove的函数节流
          clearTimeout(this.timer)
        }
        this.timer = setTimeout(() => {
          const touchY = e.touches[0].clientY - 79
          const index = Math.floor((touchY - this.startY) / 20)
          this.$emit('change', this.letters[index])
        }, 16)
      }
    }
  }
}
</script>
<style lang="stylus" scoped>
@import '~styles/variables.styl'
.alphabet
  display flex
  flex-direction column
  justify-content center
  position absolute
  top 1.58rem
  right 0
  bottom 0
  width .4rem
  .item
    color $bgColor
    line-height .4rem
    text-align center
</style>
