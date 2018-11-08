<template>
  <div class="heaer">
    <div class="container">
      <!-- 左边 -->
      <div class="logo">
        <a href="">
          <img src="https://s01.mifile.cn/i/mi-logo.png" alt="">
        </a>
      </div>
      <!-- 中间 -->
      <div class="nav">
        <div class="nav-icon">
          <img src="https://i1.mifile.cn/a4/cms_15410669089659_TZmzr.gif" alt="">
        </div>
        <div class="nav-bar">
          <a href="" v-for='(item, index) of list' :key='index'>
            <span>{{item}}</span>
          </a>
        </div>
      </div>
      <!-- 右边 -->
      <div class="search">
        <input type="text" class="search-input">
        <div class="search-icon">
          <span class="iconfont iconfont-search">&#xe608;</span>
        </div>
        <div class="search-hotwords">
          <span>小米8</span>
          <span>小米mix 2s</span>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'SiteHeader',
  props: {
    list: ''
  }
}
</script>

<style lang="stylus" scoped>
  .header
    width: 100%
  .container
    margin: 0 auto
    width: 1250px
    height: 1rems
    // -----------logo----------
  .logo
    width: 62px
    text-align: center
    height: 1rem
    line-height: 1rem
    float: left
  .logo a img
    background: #ff6700
    width: 55px
    height: 55px
    // -----------nav---------
  .nav
    float: left
    width: 850px
    height: 1rem
    line-height: 1rem
    margin-left: .1rem
  .nav .nav-icon
    width: 165px
    float:left
  .nav .nav-bar
    float: right
    width: 685px
    height: 1rem
  .nav .nav-bar a span
    font-size: 16px
    color: #333
    margin: 0 .1rem
  .nav .nav-bar a span:hover
    color: #ff6700
    //  ---------search--------
  .search
    position: relative
    float: right
    width: 2.96rem
    height: 1rem
    font-size: 14px;
    margin-top: .25rem
  .search .search-input
    display: block
    float: left
    width: 2.45rem
    height: .48rem
    line-height: .48rem
    border: 1px solid #e0e0e0;
    border-right: none
  .search .search-hotwords
    position: absolute
    right: .4rem
    top: .18rem
    width: 1.23rem
    height: .21rem
    font-size: 12px
  .search .search-hotwords span
    margin: 0 .01rem
    background: #eee
    cursor: pointer
    color: #757575
  .search .search-hotwords span:hover
    background:#ff6700
    color: #fff
  .search .search-icon
    width: .48rem
    height: .48rem
    line-height: .48rem
    border: 1px solid #e0e0e0;
    float:right
  .search .search-icon:hover
    background: #ff6700
  .search .search-icon .iconfont-search
    display: block
    text-align: center
    color: #616161
  .search .search-icon .iconfont-search:hover
    color: #fff
</style>
