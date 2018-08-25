<template>
  <div class="articles">
    <div class="art-tit">热门游记</div>
    <ul>
      <li class="border-bottom" v-for="item of articles" :key="item.id">
        <div class="item-img-wrapper">
          <img class="item-img" :src="item.imgUrl">
        </div>
        <div class="item-info">
          <p class="item-title">{{item.title}}</p>
          <p class="item-desc">{{item.desc}}</p>
        </div>
      </li>
    </ul>
  </div>
</template>
<script>
export default {
  name: 'HomeArticles',
  props: {
    articles: Array
  }
}
</script>
<style lang="stylus" scoped>
@import '~styles/mixin.styl'
.art-tit
  background #eee
  line-height .8rem
  text-indent .2rem
.item-img-wrapper
  overflow hidden
  height 0
  padding-bottom 33.9%
  img
    width 100%
.item-info
  padding .1rem
  .item-title
    line-height .54rem
    font-size .32rem
    ellipsis()
  .item-desc
    line-height .4rem
    color #ccc
    ellipsis()
</style>
