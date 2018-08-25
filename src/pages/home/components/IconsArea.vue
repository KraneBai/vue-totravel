<template>
    <div class="icons-area">
      <swiper :options="swiperOption" ref="mySwiper">
        <swiper-slide v-for="(page, index) of icons" :key="index">
          <div class="icon-item" v-for="item of page" :key="item.iconId">
            <div class="icon-img">
              <img :src="item.iconUrl">
            </div>
            <p>{{item.iconTit}}</p>
          </div>
        </swiper-slide>
      </swiper>
  </div>
</template>
<script>
export default {
  name: 'HomeIconsArea',
  props: {
    icons: Array
  },
  data () {
    return {
      swiperOption: {}
    }
  },
  computed: {
    pages () {
      const pages = []
      this.iconList.forEach((item, index) => {
        const page = Math.floor(index / 8)
        if (!pages[page]) {
          pages[page] = []
        }
        pages[page].push(item)
      })
      return pages
    }
  }
}
</script>
<style lang="stylus" scoped>
@import '~styles/variables.styl'
@import '~styles/mixin.styl'
.icons-area
  .swiper-container
    margin-top .1rem
    overflow: hidden
    height: 0
    padding-bottom: 50%
  .icon-item
    position: relative
    float: left
    width: 25%
    height: 0
    padding-bottom: 25%
    .icon-img
      position: absolute
      top: 0
      left: 0
      bottom: 0.44rem
      right: 0
      padding: 0.1rem
      box-sizing: border-box
      img
        display: block
        height: 100%
        margin: 0 auto
    p
      position: absolute
      left: 0
      right: 0
      bottom: 0
      height: 0.44rem
      line-height: 0.44rem
      text-align: center
      color: $darkTextColor
      ellipsis()
</style>
