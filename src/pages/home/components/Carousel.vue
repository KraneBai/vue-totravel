<template>
  <div class="carousel">
    <swiper :options="swiperOption" ref="mySwiper">
      <swiper-slide v-for="item of imgList" :key="item.id">
        <img :src="item.imgUrl" />
      </swiper-slide>
    </swiper>
    <div class="swiper-pagination" slot="pagination"></div>
  </div>
</template>
<script>
export default {
  name: 'HomeCarousel',
  data () {
    return {
      swiperOption: {
        pagination: {
          el: '.swiper-pagination'
        },
        loop: true
      },
      imgList: [
        {
          id: '0001',
          imgUrl: 'https://instagram.fhkg1-1.fna.fbcdn.net/vp/32c4f91132c8261c23734679b51617ba/5C3650C0/t51.2885-15/e35/14709652_1085906251527307_3848475526838616064_n.jpg'
        },
        {
          id: '0002',
          imgUrl: 'https://instagram.fhkg3-2.fna.fbcdn.net/vp/670c58b8699393fca0d8c1aa616ddbdd/5C1B2D09/t51.2885-15/e35/31920977_1004692233018995_3539427719081099264_n.jpg'
        },
        {
          id: '0003',
          imgUrl: 'https://instagram.fhkg3-2.fna.fbcdn.net/vp/78d6567c73f2282db541fa59a9792434/5C078CAF/t51.2885-15/e35/28152718_433946763707522_2555481442058502144_n.jpg'
        }
      ]
    }
  }
}
</script>
<style lang="stylus" scoped>
.carousel >>> .swiper-pagination-bullet-active
  background: #fff
.carousel
  position: relative
  overflow: hidden
  width: 100%
  height: 0
  padding-bottom: 34%
  .swiper-slide
    img
      width: 100%
  .swiper-pagination
    bottom: .1rem
    left: 50%
    transform: translateX(-50%)
</style>
