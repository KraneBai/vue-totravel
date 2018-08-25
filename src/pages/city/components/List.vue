<template>
  <div class="list" ref="wrapper">
    <div>
      <div class="area">
        <div class="title border-topbottom">当前城市</div>
        <div class="button-list">
          <div class="button-list-wrapper">
            <div class="button">北京</div>
          </div>
        </div>
      </div>
      <div class="area">
        <div class="title border-topbottom">热门城市</div>
        <div class="button-list">
          <div class="button-list-wrapper">
            <div class="button">北京</div>
          </div>
          <div class="button-list-wrapper">
            <div class="button">北京</div>
          </div>
          <div class="button-list-wrapper">
            <div class="button">北京</div>
          </div>
          <div class="button-list-wrapper">
            <div class="button">北京</div>
          </div>
          <div class="button-list-wrapper">
            <div class="button">北京</div>
          </div>
          <div class="button-list-wrapper">
            <div class="button">北京</div>
          </div>
          <div class="button-list-wrapper">
            <div class="button">北京</div>
          </div>
          <div class="button-list-wrapper">
            <div class="button">北京</div>
          </div>
          <div class="button-list-wrapper">
            <div class="button">北京</div>
          </div>
          <div class="button-list-wrapper">
            <div class="button">北京</div>
          </div>
        </div>
      </div>
      <div class="area">
        <div class="title border-topbottom">A</div>
        <div class="city-list">
          <div class="city border-bottom">安徽</div>
        </div>
      </div>
      <div class="area">
        <div class="title border-topbottom">B</div>
        <div class="city-list">
          <div class="city border-bottom">白山</div>
          <div class="city border-bottom">白城</div>
          <div class="city border-bottom">白山</div>
          <div class="city border-bottom">白山</div>
        </div>
      </div>
      <div class="area">
        <div class="title border-topbottom">C</div>
        <div class="city-list">
          <div class="city border-bottom">长春</div>
          <div class="city border-bottom">长春</div>
          <div class="city border-bottom">长春</div>
          <div class="city border-bottom">长春</div>
          <div class="city border-bottom">长春</div>
          <div class="city border-bottom">长春</div>
          <div class="city border-bottom">长春</div>
          <div class="city border-bottom">长春</div>
        </div>
      </div>
      <div class="area">
        <div class="title border-topbottom">D</div>
        <div class="city-list">
          <div class="city border-bottom">德惠</div>
        </div>
      </div>
    </div>
  </div>
</template>
<script>
import BScroll from 'better-scroll'
export default {
  name: 'CityList',
  mounted () {
    this.scroll = new BScroll(this.$refs.wrapper)
  }
}
</script>
<style lang="stylus" scoped>
.border-topbottom
  &:before
    border-color #ccc
  &:after
    border-color #ccc
.border-bottom
  &:before
    border-color #ccc
.list
  position absolute
  overflow hidden
  top 1.58rem
  left 0
  right 0
  bottom 0
  .title
    line-height .54rem
    background #eee
    padding-left .2rem
    color #666
    font-size .26rem
  .button-list
    padding .1rem .6rem .1rem .1rem
    overflow hidden
    .button-list-wrapper
      float left
      width 33.33%
    .button
      margin .1rem
      padding .1rem 0
      text-align center
      border .02rem solid #ccc
      border-radius .06rem
  .city-list
    .city
      line-height .76rem
      padding-left .2rem
</style>
