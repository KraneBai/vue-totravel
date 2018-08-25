<template>
  <div>
    <div class="banner" @click="handleShowGallary">
      <img class="banner-img" src="http://p4-q.mafengwo.net/s11/M00/E3/C2/wKgBEFsamaaATNNVABFGzrx2crA45.jpeg?imageMogr2%2Fthumbnail%2F%21440x300r%2Fstrip%2Fgravity%2FCenter%2Fcrop%2F%21440x300%2Fquality%2F90">
      <div class="banner-info">
        <div class="banner-title">「在人海」在帕劳，掉进上帝的水族箱</div>
        <div class="banner-number">
          <span class="iconfont banner-icon">&#xe614;</span>
          53
        </div>
      </div>
    </div>
    <common-gallary
      :gallaryList="gallaryList"
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
  data () {
    return {
      showGallary: false,
      gallaryList: ['http://b4-q.mafengwo.net/s10/M00/34/30/wKgBZ1jJXc6ASFxpAAhjrYZ3UWg15.jpeg?imageMogr2%2Fthumbnail%2F%21476x440r%2Fgravity%2FCenter%2Fcrop%2F%21476x440%2Fquality%2F100', 'http://p2-q.mafengwo.net/s10/M00/13/3F/wKgBZ1mvxFKAJa29AAPF2zeReW068.jpeg?imageMogr2%2Fthumbnail%2F%21640x400r%2Fgravity%2FCenter%2Fcrop%2F%21640x400%2Fquality%2F90', 'http://b2-q.mafengwo.net/s6/M00/38/DD/wKgB4lMNbkWAKYVIAAS7PpYjpiE27.jpeg?imageMogr2%2Fthumbnail%2F%21640x400r%2Fgravity%2FCenter%2Fcrop%2F%21640x400%2Fquality%2F90']
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
