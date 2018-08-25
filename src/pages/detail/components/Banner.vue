<template>
  <div>
    <div class="banner" @click="handleShowGallary">
      <img class="banner-img" :src="bannerImg">
      <div class="banner-info">
        <div class="banner-title">{{sightName}}</div>
        <div class="banner-number">
          <span class="iconfont banner-icon">&#xe614;</span>
          {{gallaryImgs.length}}
        </div>
      </div>
    </div>
    <common-gallary
      :gallaryList="gallaryImgs"
      v-show="showGallary"
      @close="handleHideGallary"
    ></common-gallary>
  </div>
</template>
<script>
import CommonGallary from 'common/gallary/Gallary'
export default {
  name: 'DetailBanner',
  components: {
    CommonGallary
  },
  props: {
    sightName: String,
    bannerImg: String,
    gallaryImgs: Array
  },
  data () {
    return {
      showGallary: false
    }
  },
  methods: {
    handleShowGallary () {
      this.showGallary = true
    },
    handleHideGallary () {
      this.showGallary = false
    }
  }
}
</script>
<style lang="stylus" scoped>
.banner
  position relative
  overflow hidden
  padding-bottom 55%
  height 0
  .banner-img
    width 100%
  .banner-info
    display flex
    position absolute
    left 0
    right 0
    bottom 0
    line-height .6rem
    color #fff
    background-image linear-gradient(top, rgba(0, 0, 0, 0), rgba(0, 0, 0, .8))
    .banner-title
      flex 1
      padding 0 .2rem
      font-size .32rem
    .banner-number
      margin-top .14rem
      padding 0 .4rem
      line-height .32rem
      height .32rem
      border-radius .2rem
      font-size .24rem
      background rgba(0, 0, 0, .8)
      .banner-icon
        font-size .24rem
</style>
