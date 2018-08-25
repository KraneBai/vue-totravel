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
      touchStatus: false
    }
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
        const startY = this.$refs['A'][0].offsetTop
        const touchY = e.touches[0].clientY - 79
        const index = Math.floor((touchY - startY) / 20)
        this.$emit('change', this.letters[index])
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
