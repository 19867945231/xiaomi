<template>
  <div>
    <div class="navbar">
      <div class="left">
        <div
          class="navitem"
          v-for="(item,index) in toplist"
          :key="index"
        >
          {{item}}
        </div>
      </div>
      <div class="right">
        <div>登录</div>
        <div>注册</div>
        <div>消息提示</div>
        <div class="carbox">购物车</div>
      </div>
    </div>
    <div class="topmiddlecontent">
      <img
        src="../static/小米logo.webp"
        alt=""
      >
      <div class="middlecontent">
        <div
          class="topitem"
          v-for="(item,index) in list"
          :key="index"
        >{{item}}</div>
      </div>
      <input
        type="text"
        placeholder="小米12"
      >
    </div>
    <!-- banner部分 -->
    <div class="banner">
      <img
        src="../static/banner.webp"
        alt=""
      >
      <!-- 左边的图片选择框 -->
      <div class="letselect">
        <div class="selectitem">手机<span>></span></div>
        <div class="selectitem">电视<span>></span></div>
        <div class="selectitem">笔记本/平板<span>></span></div>
        <div class="selectitem">出行<span>></span></div>
        <div class="selectitem">穿搭<span>></span></div>
        <div class="selectitem">音乐影像<span>></span></div>
        <div class="selectitem">家电<span>></span></div>
        <div class="selectitem">智能/路由器<span>></span></div>
        <div class="selectitem">电源/配件<span>></span></div>
        <div class="selectitem">健康/儿童<span>></span></div>
        <div class="selectitem">生活箱子<span>></span></div>
      </div>
      <!-- 商品列表 -->
      <div
        class="shop-container"
        v-show="shopshow"
      >
        <div
          class="shop-item"
          v-for="(item,index) in shoplist"
          :key="index"
        >
          <img
            :src="item.url"
            alt=""
          >
          <div class="shop-title">{{item.name}}</div>
        </div>
      </div>
    </div>
    <!-- 手机模块部分 -->
    <div class="phone-container">
      <div class="left">
        <img
          class="left-img"
          src="../static/手机.webp"
          alt=""
        >
      </div>
      <div class="right">
        <div
          class="right-item"
          v-for="(item,index) in imglist"
          :key="index"
        >
          <img
            :src="item.url"
            alt=""
          >
        </div>
      </div>
    </div>
    <div class="phone-container">
      <div class="left">
        <img
          class="left-img"
          src="../static/手机.webp"
          alt=""
        >
      </div>
      <div class="right">
        <div
          class="right-item"
          v-for="(item,index) in imglist"
          :key="index"
        >
          <img
            :src="item.url"
            alt=""
          >
        </div>
      </div>
    </div>
    <div class="phone-container">
      <div class="left">
        <img
          class="left-img"
          src="../static/手机.webp"
          alt=""
        >
      </div>
      <div class="right">
        <div
          class="right-item"
          v-for="(item,index) in imglist"
          :key="index"
        >
          <img
            :src="item.url"
            alt=""
          >
        </div>
      </div>
    </div>
    <div class="phone-container">
      <div class="left">
        <img
          class="left-img"
          src="../static/手机.webp"
          alt=""
        >
      </div>
      <div class="right">
        <div
          class="right-item"
          v-for="(item,index) in imglist"
          :key="index"
        >
          <img
            :src="item.url"
            alt=""
          >
        </div>
      </div>
    </div>
    <!-- 右边的固定定位的盒子 -->
    <div class="rightposition">
      <div class="poitem">手机</div>
      <div class="poitem">个人中心</div>
      <div class="poitem">售后服务</div>
      <div class="poitem">人工服务</div>
      <div class="poitem">购物车</div>
      <div
        v-show="isShow"
        @click="gotop"
        class="poitem"
      >回到顶部</div>
    </div>
  </div>
</template>
 
<script>
export default {
  name: "IndexPage",
  data() {
    return {
      shopshow: false,
      isShow: false,
      toplist: [
        "小米官网",
        "小米商城",
        "MIUI",
        "LOT",
        "云服务",
        "天星数科",
        "有品",
        "小爱开放平台",
        "企业团购",
        "资质证明",
        "协议规则",
        "下载APP",
        "Select Location",
      ],
      list: [
        "xiaomi手机",
        "红米手机",
        "电视",
        "笔记本",
        "平板",
        "家电",
        "路由器",
        "服务中心",
        "社区",
      ],
      shoplist: [
        { url: require("../static/banner.webp"), name: "小米9" },
        { url: require("../static/banner.webp"), name: "小米9" },
        { url: require("../static/banner.webp"), name: "小米9" },
        { url: require("../static/banner.webp"), name: "小米9" },
        { url: require("../static/banner.webp"), name: "小米9" },
        { url: require("../static/banner.webp"), name: "小米9" },
        { url: require("../static/banner.webp"), name: "小米9" },
        { url: require("../static/banner.webp"), name: "小米9" },
        { url: require("../static/banner.webp"), name: "小米9" },
        { url: require("../static/banner.webp"), name: "小米9" },
        { url: require("../static/banner.webp"), name: "小米9" },
        { url: require("../static/banner.webp"), name: "小米9" },
        { url: require("../static/banner.webp"), name: "小米9" },
        { url: require("../static/banner.webp"), name: "小米9" },
        { url: require("../static/banner.webp"), name: "小米9" },
        { url: require("../static/banner.webp"), name: "小米9" },
        { url: require("../static/banner.webp"), name: "小米9" },
        { url: require("../static/banner.webp"), name: "小米9" },
        { url: require("../static/banner.webp"), name: "小米9" },
        { url: require("../static/banner.webp"), name: "小米9" },
      ],
      imglist: [
        { url: require("../static/手机1.webp") },
        { url: require("../static/手机1.webp") },
        { url: require("../static/手机1.webp") },
        { url: require("../static/手机1.webp") },
        { url: require("../static/手机1.webp") },
        { url: require("../static/手机1.webp") },
        { url: require("../static/手机1.webp") },
        { url: require("../static/手机1.webp") },
      ],
    };
  },
  mounted() {
    window.addEventListener("scroll", this.watchscroll);
  },
  methods: {
    watchscroll() {
      // console.log("滚动了页面");
      var scrollTop =
        document.documentElement.scrollTop || document.body.scrollTop;
      // console.log(scrollTop);
      if (scrollTop > 1900) {
        this.isShow = true;
      } else {
        this.isShow = false;
      }
    },
    gotop() {
      // document.documentElement.scrollTop||document.body.scrollTop
      document.documentElement.scrollTop = 0;
    },
  },
};
</script>
<style>
.rightposition {
  position: fixed;
  right: 10px;
  top: 300px;
  line-height: 50px;
  background-color: #fff;
  text-align: center;
  z-index: 999;
}
.rightposition .poitem:hover {
  color: orangered;
  cursor: pointer;
}
.poitem {
  width: -200px;
}
* {
  margin: 0;
  padding: 0;
}
.navbar {
  display: flex;
  background-color: #333;
  line-height: 40px;
  color: #ccc;
  justify-content: space-between;
  padding: 0 100px;
  font-size: 14px;
  box-sizing: border-box;
}
.left {
  display: flex;
}
.right {
  display: flex;
}
.left .navitem {
  margin-right: 20px;
  cursor: pointer;
}
.right div {
  padding: 0 15px;
  cursor: pointer;
}
.left .navitem:hover {
  color: white;
}
.right div:hover {
  color: white;
}
.right .carbox:hover {
  background-color: #fff;
  color: black;
}
.showbox {
  width: 100px;
  height: 50px;
  background-color: #ccc;
  position: fixed;
  right: 0;
  top: 40px;
  display: none;
}
.topmiddlecontent {
  display: flex;
  justify-content: space-between;
  padding: 0 100px;
  align-items: center;
  line-height: 88px;
}
.topmiddlecontent img {
  width: 50px;
  height: 50px;
}
.topmiddlecontent .middlecontent {
  display: flex;
}
.middlecontent .topitem {
  margin-right: 10px;
}
.topmiddlecontent input {
  height: 40px;
}
.banner {
  padding: 0 100px;
  position: relative;
}
.banner img {
  width: 100%;
  height: auto;
}
.letselect {
  background-color: #ccc;
  height: 100%;
  width: 234px;
  position: absolute;
  left: 100px;
  top: 0;
  z-index: 999;
  padding: 10px 0;
  box-sizing: border-box;
}
.selectitem {
  padding: 10px 20px 10px 20px;
  display: flex;
  justify-content: space-between;
}
.selectitem:hover {
  background-color: orange;
  cursor: pointer;
  /* master分支上面的 */
}

.shop-container {
  height: 100%;
  width: 400px;
  position: absolute;
  top: 0;
  left: 335px;
  z-index: 999;
  background-color: #fff;
}
.shop-container img {
  width: 50px;
  height: 50px;
}
.shop-item {
  display: flex;
  align-items: center;
  height: 50px;
  width: 25%;
  background-color: pink;
}
.shop-container {
  display: flex;
  flex-wrap: wrap;
  width: 1084px;
  align-content: space-between;
}
.phone-container {
  padding: 0 100px;
  display: flex;
  margin-top: 30px;
}
.phone-container .right {
  display: flex;
  flex-wrap: wrap;
  align-content: space-between;
  flex: 1;
  justify-content: space-between;
}
.right .right-item {
  width: 220px;
  background-color: #fff;
  margin-right: 10px;
  height: 300px;
}
.left > img {
  width: 234px;
  height: 614px;
}
.phone-container .left {
  margin-right: 10px;
}
body {
  background-color: #ccc;
}
.right-item img {
  width: 100%;
}
</style>>

