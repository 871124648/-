<template>
  <div class="sltitle">
    <div class="flex_pro">
      <div style="width:400rpx;">
        <span class="title_pro">历史搜索</span>
      </div>
      <div class="ify-pro-right">
        <van-icon name="delete" size="18px" style="margin-top:5px;"/>
        <span>清空</span>
      </div>
    </div>
  </div>
</template>

<script>
export default {
   data(){
    return {
    }
  },
  methods:{

  }
}
</script>

<style scoped>
@import "../../app.wxss";
.sltitle{
  background:white;
  padding:25rpx 40rpx;
  margin-top:20rpx;
}
.flex_pro{
  display: flex;
  justify-content:space-between;
  align-items:center;
}
.ify-pro-right{
  width:90rpx;
  display: flex;
  justify-content:space-between;
  align-items:center;
}
.title_pro{
  color:#333333;
  font-size:34rpx;
  font-weight:900;
}
</style>
