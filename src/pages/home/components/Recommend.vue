<template>
  <div class="recommend">
    <div class="rec-tit">热销推荐</div>
    <ul>
      <router-link
        class="rec-item border-bottom"
        v-for="item of recommend"
        :key="item.id"
        tag="li"
        :to="'/detail/' + item.id"
      >
        <img class="item-img" :src="item.imgUrl">
        <div class="item-info">
          <p class="item-title">{{item.title}}</p>
          <p class="item-desc">{{item.desc}}</p>
          <button class="item-btn">查看详情</button>
        </div>
      </router-link>
    </ul>
  </div>
</template>
<script>
export default {
  name: 'HomeRecommend',
  props: {
    recommend: {
      type: Array,
      default () {
        return []
      }
    }
  }
}
</script>
<style lang="stylus" scoped>
@import '~styles/mixin.styl'
.rec-tit
  background #eee
  margin-top .2rem
  line-height .8rem
  text-indent .2rem
.rec-item
  overflow hidden
  display flex
  height 1.9rem
  .item-img
    width 1.7rem
    height 1.7rem
    padding .1rem
  .item-info
    flex 1
    padding .1rem
    min-width 0
    .item-title
      line-height .54rem
      font-size .32rem
      ellipsis()
    .item-desc
      line-height .4rem
      color #ccc
      ellipsis()
    .item-btn
      background #ff9300
      padding 0 .2rem
      margin-top .16rem
      color #fff
      border-radius .06rem
      line-height .44rem
</style>
