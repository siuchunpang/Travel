<template>
  <div>
    <div class="title">周末去哪儿</div>
    <ul>
      <router-link tag="li"
        class="item border-bottom"
        v-for="item of list"
        :key=item.id
        :to="'/detail/' + item.id"
      >
        <img class="item-img" :src="item.imgUrl">
        <div class="item-info">
          <p class="item-title">{{item.title}}</p>
          <p class="item-desc">{{item.desc}}</p>
          <button class="item-bottom">查看详情</button>
        </div>
      </router-link>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'HomeRecommend',
  props: {
    list: Array
  }
}
</script>

<style lang="stylus" scoped>
  @import '~styles/ellipsis.styl'
  .title
    margin-top .2rem
    line-height .8rem
    background #eee
    text-indent .2rem
  .item
    overflow hidden
    display flex
    height 2.46rem
    .item-img
      height 2.16rem
      width 2.16rem
      padding .2rem
    .item-info
      flex 1
      padding .1rem
      min-width 0
      .item-title
        line-height .44rem
        font-size: .32rem
        margin-top .32rem
        ellipsis()
      .item-desc
        line-height .44rem
        color #ccc
        ellipsis()
      .item-bottom
        line-height .44rem
        margin-top .2rem
        background #ff9300
        padding 0 .2rem
        border-radius .06rem
        color #fff
</style>
