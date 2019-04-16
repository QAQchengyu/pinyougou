<template>
  <div class="search">
    <div class="search_input">
      <input type="text">
      <div class="word">
        <icon type="search" size="20"></icon>
        <span>搜索</span>
      </div>
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style lang="less">
.search {
    background-color: #eb4450;
    padding: 20rpx;

    .search_input {
        background-color: #fff;
        border-radius: 3px;
        width: 100%;
        height: 60rpx;
        position: relative;

        .word {
            position: absolute;
            // display: flex;
            // align-items: center;
            top: 50%;
            left: 50%;
            transform: translate(-50%, -50%)
        }
    }

}
</style>
