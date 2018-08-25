<template>
  <div class="carousel">
    <swiper :options="swiperOption" v-if="showSwiper">
      <swiper-slide v-for="item of swiper" :key="item.id">
        <img :src="item.imgUrl" />
      </swiper-slide>
    </swiper>
    <div class="swiper-pagination" slot="pagination"></div>
  </div>
</template>
<script>
export default {
  name: 'HomeCarousel',
  props: {
    swiper: Array
  },
  data () {
    return {
      swiperOption: {
        pagination: {
          el: '.swiper-pagination'
        },
        loop: true
      }
    }
  },
  computed: {
    showSwiper () {
      return this.swiper.length
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
