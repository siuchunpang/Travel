<template>
  <div>
    <div class="banner" @click="handleBannerClick">
      <img class="banner-img" src="//img1.qunarzz.com/sight/p0/1606/a0/a0854aa4dff05b84e2.img.jpg_600x330_d1dfb067.jpg">
      <div class="banner-info">
        <div class="banner-title">珠海长隆海洋王国</div>
        <div class="banner-number">
          <span class="iconfont banner-icon">&#xe7d1;</span>
          39
        </div>
      </div>
    </div>
    <common-gallary
      :imgs="imgs"
      v-show="showGallary"
      @close="handleGallaryClose"
    ></common-gallary>
  </div>
</template>

<script>
import CommonGallary from 'common/gallary/Gallary'
export default {
  name: 'Banner',
  data() {
    return {
      showGallary: false,
      imgs: [
        'http://img1.qunarzz.com/sight/p0/1606/a0/a0854aa4dff05b84e2.img.jpg_r_800x800_31e4db21.jpg',
        'http://img1.qunarzz.com/sight/p0/1503/c7/c784a738c2a821ad.water.jpg_r_800x800_0142959c.jpg',
        'http://img1.qunarzz.com/sight/p0/1503/df/df52ada1fcc788c7.water.jpg_r_800x800_276cad3a.jpg'
      ]
    }
  },
  methods: {
    handleBannerClick() {
      this.showGallary = true
    },
    handleGallaryClose() {
      this.showGallary = false
    }
  },
  components: {
    CommonGallary
  }
}
</script>

<style lang="stylus" scoped>
  .banner
    position relative
    overflow hidden
    height 0
    padding-bottom 55%
    .banner-img
      width 100%
    .banner-info
      display flex
      position absolute
      left 0
      right 0
      bottom 0
      line-height .6rem
      color #fff
      background-image linear-gradient(top, rgba(0, 0, 0, 0), rgba(0, 0, 0, 0.8))
      .banner-title
        flex 1
        font-size .32rem
        padding 0 .2rem
      .banner-number
        height .32rem
        line-height .32rem
        margin-top 0.14rem
        padding 0 .4rem
        border-radius .2rem
        background rgba(0, 0, 0, .8)
        font-size .24rem
        .banner-icon
          font-size .24rem
</style>
