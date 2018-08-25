<template>
  <div class="header">
    <div class="header-left">
      <span class="iconfont back-icon">&#xe624;</span>
    </div>
    <div class="header-input">
      <span class="iconfont">&#xe632;</span>
      请输入城市/景点/游玩主题
    </div>
    <div class="header-right">
      {{city}}
      <span class="iconfont arrow-icon">&#xe7ff;</span>
    </div>
  </div>
</template>
<script>
export default {
  name: 'HomeHeader',
  props: {
    city: String
  }
}
</script>
<style lang="stylus" scoped>
@import '~styles/variables.styl';
.header
  display: flex
  line-height: .86rem
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
    padding-left: .2rem
    background: #fff
    height: .64rem
    line-height: .64rem
    border-radius: .1rem
    color: #ccc
  .header-right
    text-align: center
    width: 1.24rem
    .arrow-icon
      margin-top: -.1rem
      font-size: .3rem
</style>
