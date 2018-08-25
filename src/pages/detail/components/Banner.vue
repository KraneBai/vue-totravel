<template>
  <div class="banner">
    <img class="banner-img" src="http://p4-q.mafengwo.net/s11/M00/E3/C2/wKgBEFsamaaATNNVABFGzrx2crA45.jpeg?imageMogr2%2Fthumbnail%2F%21440x300r%2Fstrip%2Fgravity%2FCenter%2Fcrop%2F%21440x300%2Fquality%2F90">
    <div class="banner-info">
      <div class="banner-title">「在人海」在帕劳，掉进上帝的水族箱</div>
      <div class="banner-number">
        <span class="iconfont banner-icon">&#xe614;</span>
        53
      </div>
    </div>
  </div>
</template>
<script>
export default {
  name: 'DetailBanner'
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
