<template>
  <div class="phtitle">
    <div class="flex_pro">
      <div style="width:400rpx;">
        <span class="title_pro">排行榜</span>
      </div>
      <div class="ify-pro-right" @click="paihangClick">
        <van-icon name="bar-chart-o" size="18px" style="margin-top:5px;"/>
        <span>完整榜单</span>
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
    paihangClick(){
      var url="../rankingList/main";
      mpvue.navigateTo({url})
    }
  }
}
</script>

<style scoped>
@import "../../app.wxss";
.phtitle{
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
  width:140rpx;
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
