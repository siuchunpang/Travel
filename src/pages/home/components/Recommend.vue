<template>
  <div>
    <div class="title">周末去哪儿</div>
    <ul>
      <li class="item border-bottom" v-for="item of weekendList" :key=item.id>
        <img class="item-img" :src="item.imgUrl">
        <div class="item-info">
          <p class="item-title">{{item.title}}</p>
          <p class="item-desc">{{item.desc}}</p>
          <button class="item-bottom">查看详情</button>
        </div>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'HomeWeekend',
  data() {
    return {
      weekendList: [{
        id: '0001',
        imgUrl: 'http://img1.qunarzz.com/sight/p0/1503/b4/b4834f16bc8f8091.water.jpg_200x200_be5f7395.jpg',
        title: '珠海长隆海洋王国',
        desc: '珠海长隆海洋王国亮点：大型鲸鲨展馆，超长飞行过山车'
      }, {
        id: '0002',
        imgUrl: 'http://img1.qunarzz.com/sight/p0/1503/b4/b4834f16bc8f8091.water.jpg_200x200_be5f7395.jpg',
        title: '珠海长隆海洋王国',
        desc: '珠海长隆海洋王国亮点：大型鲸鲨展馆，超长飞行过山车'
      }, {
        id: '0003',
        imgUrl: 'http://img1.qunarzz.com/sight/p0/1503/b4/b4834f16bc8f8091.water.jpg_200x200_be5f7395.jpg',
        title: '珠海长隆海洋王国',
        desc: '珠海长隆海洋王国亮点：大型鲸鲨展馆，超长飞行过山车'
      }]
    }
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
