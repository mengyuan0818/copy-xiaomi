<template>
  <div>
    <div class="topbar">
      <div class="container">
        <div class="topbar-nav">
          <a href="" class="">小米商城</a>
          <span>|</span>
          <a href="" class="">MIUI</a>
          <span>|</span>
          <a href="" class="">LOT</a>
          <span>|</span>
          <a href="" class="">云服务</a>
          <span>|</span>
          <a href="" class="">金融</a>
          <span>|</span>
          <a href="" class="">有品</a>
          <span>|</span>
          <a href="" class="">小爱开放平台</a>
          <span>|</span>
          <a href="" class="">政企服务</a>
          <span>|</span>
          <a href="" class="">下载app</a>
          <span>|</span>
          <a href="" class="">Select Region</a>
        </div>
        <div class="topbar-cart" @mouseenter='onMouseover' @mouseleave='onMouseleave'>
          <span class="iconfont">&#xe655;</span>
          <span>购物车(0)</span>
        </div>
        <div class="topbar-info">
          <a href="" class="">登录</a>
          <span>|</span>
          <a href="" class="">注册</a>
          <span>|</span>
          <a href="" class="">消息通知</a>
        </div>
        <transition>
          <div class="cart-list" v-show='cartShow'>
            <p>购物车中还没有商品，赶紧选购吧</p>
          </div>
        </transition>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'TopBar',
  data () {
    return {
      cartShow: false
    }
  },
  methods: {
    onMouseover () {
      this.cartShow = true
    },
    onMouseleave () {
      this.cartShow = false
    }
  }
}
</script>

<style lang="stylus" scoped>
  .topbar
    width: 100%
    height: .4rem
    background: #333
    font-size: 12px
    text-align: center
  .topbar a:hover
    color: #fff
  .container
    width: 1250px
    height: .4rem
    margin: 0 auto
    position: relative
    // -------- 导航栏 ------------
  .topbar-nav
    width: 44.2%
    height: .4rem
    line-height: .4rem
    float: left
    text-align: center
  .topbar-nav a
    color: rgb(176, 176, 176)
  .topbar-nav span
    display: inline
    font-family: sans-serif
    margin: 0 .2em;
    color: #424242;
    // -------- 信息 ------------
  .topbar-info
    width: 11.4%
    height: .4rem
    line-height: .4rem
    float: right
  .topbar-info a
    color: rgb(176, 176, 176)
  .topbar-info span
    display: inline
    font-family: sans-serif
    margin: 0 .2em;
    color: #424242;
    // -------- 购物车 ------------
  .topbar-cart
    width: 9.7%
    height: .4rem
    line-height: .4rem
    float: right
    background: #424242s
    color: rgb(176, 176, 176)
  .topbar-cart:hover
    background: #fff
    color: #ff6700
    // -------- 购物车下拉菜单 ------------
  .cart-list
    width: 25.7%
    height: auto
    background: #fff
    position: absolute
    right: 0
    top: .4rem
    box-shadow: 0 2px 10px rgba(0,0,0,0.15);
  .cart-list p
    margin: .5rem auto
    // ---------购物车动画----------
  .v-enter-active, .v-leave-active
    transition: opacity .3s
  .v-enter, .v-leave-to
    opacity: 0
</style>
