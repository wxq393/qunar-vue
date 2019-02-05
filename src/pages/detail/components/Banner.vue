<template>
  <div>
    <div class="banner" @click="handleBannerClick">
      <img class="banner-img" src="//img1.qunarzz.com/sight/p0/1508/97/ea51af995c4d4de85c53855302b2f5af.water.jpg_600x330_0f634ac7.jpg" />
      <div class="banner-info">
       <div class="banner-title">
        鼓浪屿往返轮渡
       </div> 
       <div class="banner-number">
         <span class="iconfont banner-icon">&#xe7bc;</span>
         8
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
import CommonGallary from '@/common/gallary/Gallary'
export default {
  name:'DetailBanner',
  data () {
    return {
      showGallary: false,
      imgs: ['//img1.qunarzz.com/sight/p0/1409/19/adca619faaab0898245dc4ec482b5722.jpg_600x330_f922b488.jpg', '//img1.qunarzz.com/sight/p0/1708/2b/2b3b94de99c0a425a3.img.jpg_600x330_b40971b4.jpg']
    }
  },
  methods: {
    handleBannerClick () { 
      this.showGallary = true
    },
    handleGallaryClose () {
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
    position: relative
    overflow: hidden
    height: 0
    padding-bottom: 55%
    .banner-img
      width: 100%
    .banner-info
      display: flex
      position: absolute
      left: 0
      right: 0
      bottom: 0
      line-height: .6rem
      color: #fff
      background-image: linear-gradient(top, rgba(0, 0, 0, 0), rgba(0, 0, 0, 0.8))
      .banner-title
        flex: 1
        font-size: .32rem
        padding: 0 .2rem
      .banner-number
        margin-top: .15rem
        padding: 0 .5rem
        height: .32rem
        line-height: .32rem     
        border-radius: .2rem
        background: rgba(0, 0, 0, .8)
        font-size: .24rem
        .banner-icon
          font-size: .24rem  
</style>