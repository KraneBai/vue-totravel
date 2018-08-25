<template>
    <div class="icons-area">
      <swiper :options="swiperOption" ref="mySwiper">
        <swiper-slide v-for="(page, index) of pages" :key="index">
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
  data () {
    return {
      swiperOption: {},
      iconList: [
        {
          iconId: '001',
          iconUrl:
            'http://images.mafengwo.net/images/app/m/logo_gonglve_v6.png?v=20150825',
          iconTit: '马蜂窝'
        },
        {
          iconId: '002',
          iconUrl:
            'http://images.mafengwo.net/images/app/m/logo_gonglve_v6.png?v=20150825',
          iconTit: '马蜂窝'
        },
        {
          iconId: '003',
          iconUrl:
            'http://images.mafengwo.net/images/app/m/logo_gonglve_v6.png?v=20150825',
          iconTit: '马蜂窝'
        },
        {
          iconId: '004',
          iconUrl:
            'http://images.mafengwo.net/images/app/m/logo_gonglve_v6.png?v=20150825',
          iconTit: '马蜂窝'
        },
        {
          iconId: '005',
          iconUrl:
            'http://images.mafengwo.net/images/app/m/logo_gonglve_v6.png?v=20150825',
          iconTit: '马蜂窝'
        },
        {
          iconId: '006',
          iconUrl:
            'http://images.mafengwo.net/images/app/m/logo_gonglve_v6.png?v=20150825',
          iconTit: '马蜂窝'
        },
        {
          iconId: '007',
          iconUrl:
            'http://images.mafengwo.net/images/app/m/logo_gonglve_v6.png?v=20150825',
          iconTit: '马蜂窝'
        },
        {
          iconId: '008',
          iconUrl:
            'http://images.mafengwo.net/images/app/m/logo_gonglve_v6.png?v=20150825',
          iconTit: '马蜂窝'
        },
        {
          iconId: '009',
          iconUrl:
            'http://images.mafengwo.net/images/app/m/logo_gonglve_v6.png?v=20150825',
          iconTit: '马蜂窝'
        }
      ]
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
