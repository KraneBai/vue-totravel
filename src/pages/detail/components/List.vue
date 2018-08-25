<template>
  <div>
    <div
      class="list-item"
      v-for="(item, index) of detailList"
      :key="index"
    >
      <div class="item-title border-bottom">
        <!-- <span class="item-title-icon"></span> -->
        <span class="iconfont">&#xe612;</span>
        {{item.title}}
      </div>
      <div v-if="item.children">
        <detail-list :detailList="item.children" class="item-children"></detail-list>
      </div>
    </div>
  </div>
</template>
<script>
export default {
  name: 'DetailList',
  props: {
    detailList: Array
  }
}
</script>
<style lang="stylus" scoped>
.item-title
  line-height .8rem
  font-size .32rem
  padding 0 .15rem
  .item-title-icon
    position relative
    top .06rem
    left .06rem
    display inline-block
    width .36rem
    height .36rem
    margin-right .1rem
    background-size .4rem .3rem
    background-image url(http://s.qunaerzz.com/piao/image/touch/sight/detail.png) 0 -.45rem no-repeat
.item-children
  padding 0 .2rem
</style>
