<template>
  <div>
    <!-- 轮播图 -->
    <swiper class="lunbo" indicator-dots autoplay>
      <block v-for="(item, index) in detailObj" :key="index">
        <swiper-item>
          <image :src="item" class="slide-image" mode="aspcetFill" />
        </swiper-item>
      </block>
    </swiper>
    <!-- 商品信息 -->
    <div class="box">
      <div class="price">￥279</div>
      <div class="mess">
        <div class="word">婴儿床杆子圆床通用支架挂杆两用杆实木杆遮光杆支架遮光架婴儿床杆子圆床通用支架挂杆两用杆实木杆遮光杆支架遮光架</div>
        <div class="shoucang">
          <span class="iconfont icon-shoucang"></span>
          <span @click="aa">收藏</span>
        </div>
      </div>
      <div class="pass">快递：免运费</div>
    </div>
    <!-- 图文介绍 -->
    <div class="jieshao">
      <div class="title">图文介绍</div>
      <div class="msg"></div>
    </div>
    <!-- bottomtab -->
    <div class="bottom">
      <div class="callme">
        <span class="iconfont icon-service"></span>
        <span>联系客服</span>
      </div>
      <div class="cart">
        <span class="iconfont icon-gouwuche"></span>
        <span>购物车</span>
      </div>
      <div class="incart">加入购物车</div>
      <div class="buy">立即购买</div>
    </div>
  </div>
</template>

<script>
import request from "../../utils/request.js"
export default {
  data() {
    return {
      detailObj: {}
    }
  },
  methods: {
    aa(){
      wx.showShareMenu()
    }
  },
 async mounted() {
    //接受参数
    var goods_id = this.$root.$mp.query.id
    var url = "https://itjustfun.cn/api/public/v1/goods/detail"
    var res = await request.get(url,{
      goods_id:goods_id
    })
    this.detailObj = res.data.data
    console.log(res.data.data);
    
  },
}
</script>

<style scoped lang="less">
@import "./index.less";
</style>
