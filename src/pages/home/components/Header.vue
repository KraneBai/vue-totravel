<template>
  <div class="header">
    <!-- <div class="header-left">
      <span class="iconfont back-icon">&#xe624;</span>
    </div> -->
    <div class="header-input">
      <span class="iconfont">&#xe632;</span>
      请输入城市/景点/游玩主题
    </div>
    <router-link to="/city">
      <div class="header-right">
        {{city}}
        <span class="iconfont arrow-icon">&#xe7ff;</span>
      </div>
    </router-link>
  </div>
</template>
<script>
import { mapState } from 'vuex'
export default {
  name: 'HomeHeader',
  computed: {
    ...mapState(['city'])
  }
}
</script>
<style lang="stylus" scoped>
@import '~styles/variables.styl'
@import '~styles/mixin.styl'
.header
  display: flex
  line-height: $headerHeight
  background: $bgColor
  color: #fff
  align-items: center
  .header-left
    width: .64rem
    text-align: center
    .back-icon
      font-size: .4rem
  .header-input
    flex: 1
    margin-left .2rem
    padding-left: .2rem
    background: #fff
    height: .64rem
    line-height: .64rem
    border-radius: .1rem
    color: #ccc
  .header-right
    margin-left .1rem
    text-align center
    min-width 1.24rem
    color #fff
    .arrow-icon
      right .05rem
      font-size: .3rem
</style>
