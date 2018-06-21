<template>
    <div class="header">
        <div class="m-top-bar editable">
            <div class="container">
                <ul class="fl">
                    <li class="fl J_login_status dn nologin">
                        <a class="menu-item fl J_do_login J_chgurl" href="#">
                            <span>Hi,请登录</span>
                        </a>
                        <a class="menu-item fl ht" href="#">免费注册</a>
                    </li>
                    <li class="fl J_login_status dn islogin" v-show="hide">
                        <a href="#" class="userinfo" target="self"></a>
                        <a href="#" style="margin:0 10px" title="退出" target="self">退出</a>
                    </li>
                    <li class="fl sep"></li>
                </ul>
                <ul class="fr bar-right">
                    <li class="fl dropdown my-feiniu">
                        <a class="menu-item" href="#" target="blank">
                            <span>我的商城</span>
                            <i class="dd"></i>
                        </a>
                        <ul class="sub-panel" v-show="hide">
                            <li>
                                <a class="J_chgurl" href="#">我的订单</a>
                            </li>
                            <li>
                                <a class="J_chgurl" href="#">我的积分</a>
                            </li>
                            <li>
                                <a class="J_chgurl" href="#">我的优惠券</a>
                            </li>
                            <li>
                                <a class="J_chgurl" href="#">我的收藏夹</a>
                            </li>
                            <li>
                                <a class="J_chgurl" href="#">我的评论</a>
                            </li>
                        </ul>
                    </li>
                    <li class="fl sep"></li>
                    <li class="my-cart fr" id="hd-my-cart">
                        <p class="c-num fl quantity">
                            <span class="count cart_quantity" id="cart_quantity"></span>
                            <i class="i-c oh"></i>
                        </p>
                        <div id="show_minicart" class="sub-panel u-fn-cart u-mn-cart">
                            <div id="minicart" class="minicartContent">

                            </div>
                        </div>
                    </li>
                    <li class="fl sep"></li>
                    <li class="fl">
                        <a class="menu-item" href="#" target="blank">
                            <span>帮助中心</span>
                        </a>
                    </li>
                    <li class="fl sep"></li>
                    <li class="fl about-us">
                        <a class="txt fl" style="line-height:unset" href="">关注我们：</a>
                    </li>
                    <li class="fl dropdown weixin">
                        <a href="" class="fl ico"></a>
                        <div class="sub-panel wx-box" v-show="hide">
                            <!-- <span class="arrow-b">◆</span>
                            <span class="arrow-a">◆</span> -->
                            <p class="n"> 扫描二维码
                                <br>关注官方微信</p>
                            <img src="" alt="微信二维码">
                        </div>
                    </li>
                </ul>
            </div>
        </div>

        <div class="m-top-sidebar m-sdb-sale J-sdb" style="z-index:401;" v-show="hide">
            <div class="t-main">
                <div class="tb-tabs">
                    <div class="tb-tabs-up">
                        <a class="i-cart" href="">
                            <span class="text">购物车</span>
                            <span id="miniCartRightQty" class="num"></span>
                        </a>
                        <a href="" target="blank" class="i-ico i-ico-order">
                            <span>我的订单</span>
                            <i class="demo-icon"></i>
                        </a>
                        <a href="" target="blank" class="i-ico i-ico-coupon">
                            <span>我的优惠券</span>
                            <i class="demo-icon"></i>
                        </a>
                        <a href="" target="blank" class="i-ico i-ico-fav">
                            <span>我的收藏</span>
                            <i class="demo-icon"></i>
                        </a>
                        <a href="" target="blank" class="i-ico i-ico-foot">
                            <span>我的评论</span>
                            <i class="demo-icon"></i>
                        </a>
                    </div>
                    <div class="tb-tabs-down">
                        <a href="" target="blank" class="i-ico i-ico-ur">
                            <span>意见反馈</span>
                            <i></i>
                        </a>
                        <a href="" class="i-ico i-ico-gotop">
                            <em></em>
                            <span>返回顶部</span>
                            <i></i>
                        </a>
                    </div>
                    <div class="my-cart-shim"></div>
                </div>
                <div class="my-cart">
                    <div class="mn-c-top">
                        <a href="">我的购物车</a>
                        <i></i>
                    </div>
                    <div class="sub-panel u-fn-cart u-mn-cart">
                        <div id="miniCartRight"></div>
                        <div class="empty-c fn-hide">
                            <span class="ma">
                                <i class="c-i oh"></i>购物车中没有商品
                            </span>
                        </div>
                    </div>
                </div>
            </div>
        </div>
        <div class="m-top-bgi">
            <div class="m-top-search editable">
                <div class="container">
                    <div class="m-top-search-form fl">
                        <form name="sourch_form" id="sourch_form" method="post" action="">
                            <div class="s-form">
                                <i class="s-ico"></i>
                                <input type="text" autocomplete="off" class="fl s-input" name="q" id="q" value="" placeholder="搜索关键字">
                                <a href="" class="s-btn fl" onclick="">搜索</a>
                            </div>
                            <div class="s-hotword">
                                
                            </div>
                            <ul class="s-tip-list"></ul>
                        </form>
                    </div>
                    <div class="logo fl">
                        <a href="/" class="item fl">
                            <img width="100px" height="auto" src="" alt="logo">
                        </a>
                    </div>
                </div>
            </div>
        
            <div class="m-top-nav editable">
                <div class="main-container new-year">
                    <ul class="main-nav">
                       <li class="nav-item">
                           <a class="menu-item menu-item-active" href="" >首页</a>
                       </li>
                     </ul>
                 </div>
             </div>
        </div>
    </div>
</template>

<script>
export default {
  name: "ComHeader",
  data() {
      return {

      };
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
body{
    margin:0;
    padding: 0;
    width: 100%;
}
li {
    display: inline-block;
    text-decoration: none;
}
a {
    text-decoration: none;
}
.header {
    width:100%;
    height: auto;
    max-height: 180px;
    
}
.m-top-bar {
    width: 100%;
}
.m-top-bar .container {
    width: 80%;
    height:30px;
    position: relative;
    margin: 0 auto;
    background-color: #fff;
}
.m-top-bar .container .fl{
    height: 30px;
    float: left;
} 

.m-top-bar .container .fr{
    height: 30px;
    float:right;
}
.container .fr .sub-panel {
    
}
.m-top-bar .container .fr .sub-panel li{
    display: block;
    position: relative;
    width: 70px;
    height: 20px;
    line-height: 20px;
}
li,a{ 
    color: #777;
    font-size: 13px;
}
.m-top-bgi {
    width: 100%;
    height:160px;
    background-color: #2a1a2b;
}
</style>
