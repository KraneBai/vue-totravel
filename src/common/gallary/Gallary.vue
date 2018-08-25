<template>
  <div class="gallary" @click="hideGallary">
    <div class="wrapper">
      <swiper :options="swiperOption">
        <swiper-slide v-for="(item, index) in gallaryList" :key="index">
          <img class="gallary-img" :src="item" />
        </swiper-slide>
        <div class="swiper-pagination" slot="pagination"></div>
      </swiper>
    </div>
  </div>
</template>
<script>
export default {
  name: 'CommonGallary',
  props: {
    gallaryList: {
      type: Array,
      default () {
        return []
      }
    }
  },
  data () {
    return {
      swiperOption: {
        pagination: {
          el: '.swiper-pagination',
          type: 'fraction'
        },
        // 我这个元素或者父级元素发生dom结构变化时，自我刷新，解决宽度计算的问题
        observeParents: true,
        observer: true
      }
    }
  },
  methods: {
    hideGallary () {
      this.$emit('close')
    }
  }
}
</script>
<style lang="stylus" scoped>
.gallary >>> .swiper-container
  overflow inherit
.gallary
  display flex
  flex-direction column
  justify-content center
  position fixed
  top 0
  left 0
  bottom 0
  right 0
  z-index 99
  background #000
  .wrapper
    width 100%
    height 0
    padding-bottom 100%
    .gallary-img
      width 100%
    .swiper-pagination
      color #fff
      bottom -1rem
</style>
