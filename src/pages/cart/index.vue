<template>
  <div>
    <!-- 收货地址 -->
    <div class="address">
      <!-- 没有选择地址的状态 -->
      <div v-if="address != null ? true : false" class="no-address">
        <div class="word">请选择收货地址</div>
        <div class="iright">
          <span class="iconfont iconright"></span>
        </div>
      </div>
      <!-- 选择地址后的状态 -->
      <div v-else class="yes-address">
        <div class="uname">
          <div class="name">
            收件人： 小追命
          </div>
          <div class="phone">
            13800000000<span class="iconfont iconright"></span>
          </div>
        </div>
        <div class="uadress">
          深圳市宝安区幸福路快乐街28号
        </div>
      </div>
      <img class="img" src="../../../static/images/cart_border@2x(1).png" alt="">
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      address: null
    }
  }
}
</script>

<style scoped lang="less">
@import './index.less';
</style>
