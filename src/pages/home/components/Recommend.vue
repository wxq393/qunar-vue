<template>
  <div>
    <div class="title">猜你喜欢</div>
    <ul>
      <li class="item border-bottom" 
          v-for="item of list" 
          :key="item.id"
      >
        <img class="item-img" :src="item.imgUrl" />
        <div class="item-info">
          <p class="item-title">{{item.title}}</p>
          <p class="item-desc">{{item.desc}}</p>
          <button class="item-button">查看详情</button>
        </div>       
      </li>
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
  @import '~styles/mixins.styl'
  .title
    margin-top: .2rem
    line-height: .8rem
    background: #eee
    text-indent: .2rem
  .item
    overflow: hidden
    display: flex
    height: 2rem

    .item-img
      widtd: 2rem
      height: 2rem
      padding: .1rem
    .item-info
      flex: 1
      padding: .1rem
      min-width: 0
      .item-title
        line-height: .66rem
        font-size: .36rem
        ellipsis()
      .item-desc
        line-height: .7.5rem
        color: #ccc
        ellipsis()
      .item-button
        line-height: .55rem
        margin-top: .3rem
        background: #ff9300
        padding: 0 .2rem
        border-radius: .06rem
        color: #fff       
</style>